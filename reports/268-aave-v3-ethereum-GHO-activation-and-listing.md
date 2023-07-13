# Proposal 268. Aave v3 Ethereum - activation of GHO and listing

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=268](https://app.aave.com/governance/proposal/?proposalId=268)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-mainnet-launch/13574](https://governance.aave.com/t/arfc-gho-mainnet-launch/13574)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:walking: gho

<br>

### Context

This proposal actives the GHO stablecoin, by configuring the first two entities with permissions to mint it (facilitators): Aave v3 Ethereum and the FlashMinter smart contract.

Activating the Aave v3 Ethereum facilitator implies a custom listing of GHO as a borrowable asset on the pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x06d612492eb2b8b0a64ac47d87fb7e2569814c62a5b5b3c0018edb464808740e](https://etherscan.io/tx/0x06d612492eb2b8b0a64ac47d87fb7e2569814c62a5b5b3c0018edb464808740e)

```
- id: 268
- creator: 0x1c037b3c22240048807cc9d7111be5d455f640bd
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x16765d275c00caa7ec9a30d1629fd42121c3ae6b]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17672941
- endBlock: 17692141
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xd7580c21b6d05a867f7647708042af1766bc774a67c440eedca1f3a5589900e7
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/268.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/268.md)


<br>

### Technical analysis


[Proposal payload](https://etherscan.io/address/0x16765d275c00caa7ec9a30d1629fd42121c3ae6b#code#F1#L75)

**Highlights**

- The proposal uses a counterfactual deployment approach for GHO and the FlashMinter facilitator contract, via CREATE2. This is correct (even if most probably not necessary), and only causes uncertainty if said contracts will be deployed by the Aave Level 1 Executor (Short) via the payload, or by any other entity in advance. In any case, the address for `GHO` will be `0x40d16fc0246ad3160ccc09b8d0d3a2cd28ae6c2f` and for `FlashMinter` `0xb639D208Bcf0589D54FaC24E655C79EC529762B8`
- GHO is a pretty special listing, with custom aToken and debtTokens, which work differently than any other listing, not respecting (purposely) certain invariants of the protocol. The main one is that external users don't deposit GHO into the protocol to make it borrowable, or to use it as collateral: when users of Aave v3 Ethereum will borrow GHO, this will be minted on demand.
Certain listing configurations are consequence of this special nature:
  - Caps don't apply. GHO can't be deposited into Aave, so there is no supply cap. Regarding borrow cap, the one of the pool doesn't apply, as the bucket size of Aave v3 Ethereum as GHO facilitator already serves as cap.
  - GHO can't be used as collateral. Same reason as before, GHO doesn't get supplied to Aave.
- The payload has different `require` that are superfluous, but acceptable as a way of being explicit on proper configurations.



In terms of actions, we have verified the payload does the following:
1. Deploys the GHO token, or skips it if the counterfactual address already has bytecode content. Then, validates the super admin of GHO (`DEFAULT_ADMIN_ROLE`) and grants `FACILITATOR_MANAGER_ROLE` and `BUCKET_MANAGER_ROLE` to the Aave Governance Level 1 Executor.
2. Deploys the FlashMinter contract, or skips it if the counterfactual address already has bytecode content. Then, validates its configuration: the flash mint fee is 0, the GHO token configured there is the correct GHO address, the Gho treasury is the Aave Ethereum Collector and the addresses provider configured is the Aave v3 Ethereum addresses provider.
3. Configures the price feed for GHO on the AaveOracle to [a smart contract returning fixed amount 1 USD](https://etherscan.io/address/0xD110cac5d8682A3b045D5524a9903E031d70FCCd#code), respecting Chainlink format (8 decimals precision) and interface for Aave (`latestAnswer()`).
4. Next, it lists GHO on Aave, by calling `initReserves()` on the Aave v3 Ethereum Pool Configurator, and enables it to borrow by calling `setReserveBorrowing()` on the same contract. As previously mentioned, GHO uses custom a/v Token smart contracts, on which we will not go into details, as they have been audited by the security providers of the community. The interest rates strategy is also custom, but respects the required interface by Aave v3.
5. With the addresses of the aToken and variable debt token proxies, different ad-hoc parameters are configured on them, like connecting the aToken to the variable debt token, and viceversa; connecting a discount rate strategy contract to the variable debt token, or setting up the GHO treasury parameter on the aToken (to be the Aave Ethereum Collector).
6. Afterwards, the `setGHODebtToken()` function on stkAAVE is called, to connect the variable debt token of GHO, in order to properly account for the discount dynamics when holding stkAAVE and borrowing.
7. Finally, both the GHO aToken (representing Aave v3 Ethereum) and FlashMinter are enabled as facilitators of GHO, by giving buckets sizes of 100'000'000 GHO and 2'000'000 GHO, respectively.

The configuration steps and parameters are aligned with the forum discussions and Snapshots.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

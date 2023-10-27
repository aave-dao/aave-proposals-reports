# Proposal 352. Treasury Management - Enhance incentives strategy on Balancer
<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=352](https://app.aave.com/governance/proposal/?proposalId=352)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-enhancing-aave-daos-liquidity-incentive-strategy-on-balancer/15061](https://governance.aave.com/t/arfc-enhancing-aave-daos-liquidity-incentive-strategy-on-balancer/15061)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposals executes aUSDC (v3 Ethereum) and AAVE OTC deals for AURA, and releases the proceeds of these deals to the GHO Liquidity Commitee, together with extra aUSDC (for more AURA buys) and veBAL.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0685b3dcff31d74f86f81f6fb126450ca62f5530a22ce19aef876639f31e7218](https://etherscan.io/tx/0x0685b3dcff31d74f86f81f6fb126450ca62f5530a22ce19aef876639f31e7218)

```
- id: 352
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x20a067bf6956996c7c8b7a98073a9d260db03b7a]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18420074
- endBlock: 18439274
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x7838470b01b15dd9753eed62747a8c6b69161b6df57b428a12b3664911f783c2
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/352.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/352.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x20a067bf6956996c7c8b7a98073a9d260db03b7a#code#F1#L29) does the following:
1. Executed an OTC deal of 200'000 aUSDC (v3 Ethereum) and 2'965 AAVE for 477'088 AURA with the Aura DAO. Technically, this is done by transferring the AURA from the Aura treasury address, and sending USDC (post-redeem) and AAVE to the Aura ecosystem fund.
2. Redeem 400'000 aUSDC (v2 Ethereum) to USDC, and send it to the GHO Liquidity Commitee.
3. Send all holdings of veBAL to GLC, to progress on the incentives strategy on Balancer. 


The payload *is not completely consistent with the AIP description, governance forum and Snapshot*, but we don't think it implies any meaningful risk for the Aave DAO.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

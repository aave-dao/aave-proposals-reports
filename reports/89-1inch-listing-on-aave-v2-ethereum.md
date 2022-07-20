# Proposal 89. Add 1INCH to Aave V2 Ethereum

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=89](https://app.aave.com/governance/proposal/?proposalId=89)

or

[https://bafybeidgixvkuyabq3g6xh3qyegzqg3fah5mj7fap7nsnqtsknqpmgczye.ipfs.infura-ipfs.io/governance/proposal/89/](https://bafybeidgixvkuyabq3g6xh3qyegzqg3fah5mj7fap7nsnqtsknqpmgczye.ipfs.infura-ipfs.io/governance/proposal/89/)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-add-1inch-as-collateral/8056](https://governance.aave.com/t/arc-add-1inch-as-collateral/8056)

<br>

## BGD analysis

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists the [1INCH](https://etherscan.io/address/0x111111111117dc0aa78b770fa6a738034120c302) asset on Aave V2 Ethereum.

**IMPORTANT** We are aware that there was a misconfiguration on the IPFS's proposal description while doing the creation, and the proposer plans to cancel and re-create with exactly the same proposal payload.
Apart from that issue on the description, there is no problem on the proposal, but we agree that it is better for the community to have the full 3 days of voting via all the available interfaces (including the Aave UI).

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9e7fcf51dd16b327dd80444d0e05a77bcc06c4993dd28edbcd63eb9e4e5196df](https://etherscan.io/tx/0x9e7fcf51dd16b327dd80444d0e05a77bcc06c4993dd28edbcd63eb9e4e5196df)

```
- id: 89
- creator: 0xd2362dbb5aa708bc454ce5c3f11050c016764fa6
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd417d07c20e31f6e129fa68182054b641fbec8bd]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15175998
- endBlock: 15195198
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x12f2d9c91e4e23ae4009ab9ef5862ee0ae79498937b66252213221f04a5d5b32
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/089.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/089.md)

<br>

### Technical analysis

This proposal lists the 1INCH token on Aave V2 Ethereum as borrowing asset and collateral, via the proposal payload [OneInchListingPayload](https://etherscan.io/address/0xd417d07c20e31f6e129fa68182054b641fbec8bd#code).

We have verified that the listing parameters are consistent with the ones pre-approved on [Snapshot](https://snapshot.org/#/aave.eth/proposal/0x2ea76814a0dfcad7ea1a7b3c597f059a8d574f8143886b23043918998505f5a7), being:

- **LTV**: 40%
- **Liquidation Threshold**: 50%
- **Liquidation Bonus**: 8.5%
- **Reserve Factor**: 20%
- **Enabled to borrow**.
- **Not enabled to borrow at stable mode**.

Some remarks from BGD:

- 1INCH properly reuses an interest rate strategy defining the exact same parameters.
- We have verified that the implementations used for aToken, variableDebtToken and stableDebtToken are the same as existing ones for other assets listed.
- We have verified that, before the listing itself, the 1INCH/ETH feed is correctly configured on the Aave oracle.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:x: BGD reviewed the procedure followed to submit the proposal.

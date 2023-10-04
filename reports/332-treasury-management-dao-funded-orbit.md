# Proposal 332. Treasury Management - DAO funded Orbit (delegation compensation program)

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=332](https://app.aave.com/governance/proposal/?proposalId=332)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-expansion-of-orbit-a-dao-funded-delegate-platform-initiative/14785](https://governance.aave.com/t/arfc-expansion-of-orbit-a-dao-funded-delegate-platform-initiative/14785)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal transitions the [Orbit delegate platform funding](https://governance.aave.com/t/introducing-orbit-a-delegate-platform-funding-initiative-by-aci/13241) initiated by ACI to being fully governance-controlled and funded.

In practise, it will create a series of 90-days 15'000 GHO streams from the Aave Collector to the top-participating delegate platforms.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x86a9a16dec21dd1ebe3cf2a9e552b139bb2d1ff5598afaca70be5fbb45a8d8e0](https://etherscan.io/tx/0x86a9a16dec21dd1ebe3cf2a9e552b139bb2d1ff5598afaca70be5fbb45a8d8e0)

```
- id: 332
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x390000ed3d6289fbfeb1af663a9812a1001573b7]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18249113
- endBlock: 18268313
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xade079d8319f8290a121a2b50ceb0cb85e7438eb0bdb5df78e7d52682c8b4f5c
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/332.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/332.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x390000ed3d6289fbfeb1af663a9812a1001573b7#code#F1#L14) properly creates five 90-day GHO streams from the Aave Collector to the each one of the selected delegate platforms: StableLab, Keyrock, LBS Blockchain, HKUST and Michigan.


The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

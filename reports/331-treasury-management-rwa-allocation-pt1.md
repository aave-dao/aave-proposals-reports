# Proposal 331. Treasury Management - RWA allocation for Centrifuge, part 1

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=331](https://app.aave.com/governance/proposal/?proposalId=331)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-treasury-rwa-allocation/14790](https://governance.aave.com/t/arfc-aave-treasury-rwa-allocation/14790)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal initiates the process of the Aave Collector investing in RWAs, by releasing an initial setup budget of 50'000 USDC to Centrifuge.

Additionally, a stream of 500 AAVE during 2 years is created as compensation to Centrifuge.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x2ca947321b29333e983b184c146acc10a102bd84efd5794c179d01a2dee70608](https://etherscan.io/tx/0x2ca947321b29333e983b184c146acc10a102bd84efd5794c179d01a2dee70608)

```
- id: 331
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xfd6933aedc23fcba8b52de85d2abfe6c93ef6f75]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18249091
- endBlock: 18268291
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x6be4bbc3c31295b1f77832d14a45bc8c85e9e159305e5d9ddb1f9fde279ae588
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/331.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/331.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xfd6933aedc23fcba8b52de85d2abfe6c93ef6f75#code#F1#L15) does the following:


1. Withdraw 50'000 aUSDC from the Aave Ethereum Collector.

2. Redeem USDC from aUSDC.

3. Transfer the USDC to Centrifuge address.

4. Create a 2 years stream of AAVE, to the Centrifuge address.

The proposal is consistent with the description in the forum and Snapshot.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

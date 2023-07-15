# Proposal 269. Aave v3 Ethereum, Optimism - caps update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=269](https://app.aave.com/governance/proposal/?proposalId=269)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gauntlet-supply-cap-updates-for-ethereum-v3-optimism-v3-2023-07-05/13917](https://governance.aave.com/t/arfc-gauntlet-supply-cap-updates-for-ethereum-v3-optimism-v3-2023-07-05/13917)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal decreases supply of different assets on Aave v3 Ethereum and Optimism, procedure that is not covered at the moment by Risk Stewards (only increase).


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x90d542222c7ccdcafee18157741512223b9d21c50591ff94f141072e9875c5f2](https://etherscan.io/tx/0x90d542222c7ccdcafee18157741512223b9d21c50591ff94f141072e9875c5f2)

```
- id: 269
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x2ee993533a482fe0f22d0fdf1b84ae1a0537e5ed,0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0,0]
- signatures: [execute(),execute(address)]
- calldatas: [0x,0x000000000000000000000000e1dd796dbeb5a67ce37cbc52dcd164d0535c901e]
- withDelegatecalls: [true,true]
- startBlock: 17674024
- endBlock: 17693224
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x73fbf4d3b8dd87a2dd8d28ad0a6ca5b20a1767391950e07fe763d2d59d3af5ad
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/269.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/269.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/269_Optimism_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/269_Optimism_pending_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system in the part that communicates with Aave on Optimism.

Regarding the payloads, they do the following:

**[Ethereum payload](https://etherscan.io/address/0x2ee993533a482fe0f22d0fdf1b84ae1a0537e5ed#code#F1#L14)**

The payload changes the following caps:

BAL
- Supply cap: 700'000 BAL -> **350'000 BAL**

LINK
- Supply cap: 24'000'000 LINK -> **15'000'000 LINK**


**[Optimism payload](https://optimistic.etherscan.io/address/0xe1dd796dbeb5a67ce37cbc52dcd164d0535c901e#code#F1#L34)**

The payload changes the following caps:

OP
- Supply cap: 20'000'000 OP -> **10'000'000 OP**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

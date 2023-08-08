# Proposal 287. Treasury Management - cancel and replace Llama streams

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=287](https://app.aave.com/governance/proposal/?proposalId=287)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-cancel-llama-service-provider-stream/14137](https://governance.aave.com/t/arfc-cancel-llama-service-provider-stream/14137)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

Following the events described on the governance forum, this proposal cancels Llama's aUSDC (v2) and AAVE current streams, to replace them with 2 new ones for half the amount during their pending engagement duration (57 days).


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb2361b77bf0bc38c810f868bb2ffb7ba555a47605d01181ba9f972c7dab48865](https://etherscan.io/tx/0xb2361b77bf0bc38c810f868bb2ffb7ba555a47605d01181ba9f972c7dab48865)

```
- id: 287
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5ae34639f76ddf430850589c9e9189b013fa2b6c]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17849634
- endBlock: 17868834
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xc7c9a8a16f30f2836e49ddb7382629e7bbb3e34d85016bb966e42c5167954a9e
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/287.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/287.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x5ae34639f76ddf430850589c9e9189b013fa2b6c#code) does the following:

1. Cancels streams `100003` of aUSDC (v2) in the Aave Ethereum Collector, and `100001` of AAVE in the Aave Ecosystem Reserve. We checked they are effectively belonging to Llama.

2. Creates 2 new streams, of 57 days (in seconds): 54'659.61 aUSDC (v2)  and 283.23 AAVE in the Aave Ecosystem Reserve.
We have verified these amounts are aligned with the forum description.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

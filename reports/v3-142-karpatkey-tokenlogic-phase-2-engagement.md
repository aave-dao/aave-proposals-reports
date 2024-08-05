# Proposal 142. TokenLogic + karpatkey - Phase II.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=142](https://vote.onaave.com/proposal/?proposalId=142)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-tokenlogic-karpatkey-financial-service-providers-phase-ii/18285](https://governance.aave.com/t/arfc-tokenlogic-karpatkey-financial-service-providers-phase-ii/18285)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x8e63E94375a51541507E6a0C70bfd417D4e2C0FF#code#F1#L43)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

:bank: payment stream

<br>

### Context

This AIP proposes a 6 months extension to Karpatkey & TokenLogin's engagement as service providers.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4f230302e77d9cc4fb529f0827ef256c2eb2ebf9d43b14c8441594d9fd53d4a0](https://etherscan.io/tx/0x4f230302e77d9cc4fb529f0827ef256c2eb2ebf9d43b14c8441594d9fd53d4a0)

```
- proposalId: 142
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x32dc0cd9bb6976c0f32ecbab0b7261298dd693f5fdf4fbfd8c9eba77718554a9
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "153" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x32dc0cd9bb6976c0f32ecbab0b7261298dd693f5fdf4fbfd8c9eba77718554a9" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/142.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/142.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/153.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/153.md)

<br>

### Technical analysis

We have verified that the payload executes the following actions:

- Transfers an equal sum of GHO to both Karpatkey and TokenLogic for the period passed since the end of the previous commitment until the execution of the proposal. The total sum transferred is ~67k GHO each, calculated as the fraction of time since phase 1 end until execution from 250k GHO uniformly distributed over 6 months of the new engagement.

- Creates an equal payment stream of GHO to both Karpatkey and TokenLogic, for the sum of 250k minus the already transferred amount, for a period beginning at execution and ends 6 months since the end of phase 1 (December 15, 2024).

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

# Proposal 238.  wstETH Borrow Rate + rsETH Supply Cap Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=238)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-prime-instance-wsteth-borrow-rate-rseth-supply-cap-update/20644)

### Payloads

* Ethereum Lido - [proposal payloads](https://etherscan.io/address/0x1D750858e8203a553b2368fb0d461Aa9d511Caa9)


## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
This publication proposes reducing the wstETH Slope1 and increasing the rsETH Supply Cap.

### Proposal Creation
Transaction: [0x3ee3719fda3c7ba17b35e9f02a9eeb3c54f09480c732e15e1e0dc520bba7a1ba](https://etherscan.io/tx/0x3ee3719fda3c7ba17b35e9f02a9eeb3c54f09480c732e15e1e0dc520bba7a1ba)
- `proposalId`: 238
- `creator`: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x2479e1a8a5b3e4d8023d061ade4a187ee9da5e17d7c91b8ed0a3e71522dd33d0

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "238" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x2479e1a8a5b3e4d8023d061ade4a187ee9da5e17d7c91b8ed0a3e71522dd33d0" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/238.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/238.md)


### Technical Analysis
We have verified the parameters configured correctly with respect to their decimals (75 -> 0.75). 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
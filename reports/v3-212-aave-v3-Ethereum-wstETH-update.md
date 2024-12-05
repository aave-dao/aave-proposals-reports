# Proposal 212. wstETH Reserve Update

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=212](https://vote.onaave.com/proposal/?proposalId=212)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-prime-core-instance-wsteth-reserve-update/19973](hhttps://governance.aave.com/t/arfc-prime-core-instance-wsteth-reserve-update/19973)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x6da115AD59F6106e1132E5835bEf300c8D429f0C#code#F1#L1)

* Ethereum Lido - [proposal payloads](https://etherscan.io/address/0x697C58E6505e70f266707b035F0b26890682B612#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

The proposal aims to adjust the interest rate parameters for the wstETH Reserve on both the Core and Lido instances of Aave v3 to enhance capital efficiency and support increased user demand. By modifying the Uoptimal and other rate parameters, the proposal seeks to better align with current liquidity utilization and encourage user retention following changes in external rewards.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xdd70436b624b077595c9912551698b991b15e90ba745f207a8ae89e84e139f9d](https://etherscan.io/tx/0xdd70436b624b077595c9912551698b991b15e90ba745f207a8ae89e84e139f9d)

```
- proposalId: 212
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x6a920a300a657492ff4dd7bdf16ac369e95db677c3139977803c75ca0f8489d1
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
      "payloadId": "216" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x6a920a300a657492ff4dd7bdf16ac369e95db677c3139977803c75ca0f8489d1" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/212.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/212.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/216.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/216.md)

<br>

### Technical analysis

During the technical analysis of the proposal to update the wstETH Reserve parameters on Aave v3, we identified a discrepancy between the forum discussion and the Solidity payload for the Lido instance. Specifically, the forum proposed setting the Uoptimal (optimal utilization rate) to 80%, while the payload and IPFS document set it at 90%. To address this inconsistency, the plan is to utilize the Aave Risk Steward to modify the Uoptimal value back to 80% after the payload is executed, ensuring alignment with the original intent. Additionally, we have thoroughly reviewed all other parameters in the proposal and confirmed that they match correctly between the documentation and the payload. By ensuring all parameters are accurate, the proposal effectively supports capital efficiency and user retention as intended. This approach maintains consistency in risk parameters while accommodating necessary updates post-execution.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


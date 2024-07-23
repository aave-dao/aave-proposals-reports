# Proposal 131. Increase CCIP Facilitator Capacity.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=131](https://vote.onaave.com/proposal/?proposalId=131)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-arb-increase-ccip-facilitator-capacity/18169](https://governance.aave.com/t/arfc-gho-arb-increase-ccip-facilitator-capacity/18169)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xc56F97A9eD9241868edcae701E55f8541B684931#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x126beE0FD953531be0dcA46c4c9e54745A29686a#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal suggests to increase the bucket capacity and bridgeLimit of the CCIP facilitator to 2.5M GHO due to the facilitator reaching full capacity.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xfe1f6c9b617c569656b35fdbd0a2a7f33f6c989791f2fabf13c22fcb4722d673](https://etherscan.io/tx/0xfe1f6c9b617c569656b35fdbd0a2a7f33f6c989791f2fabf13c22fcb4722d673)

```
- proposalId: 131
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x6bea4d8ce7ba6bf63552fcdfed79641f76ec8c9a09c482aef53ab997432ac9aa
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
      "payloadId": "145" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "38" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x6bea4d8ce7ba6bf63552fcdfed79641f76ec8c9a09c482aef53ab997432ac9aa" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/131.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/131.md)

**Payload reports**

* Ethereum - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/145.md)

* Arbitrum - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/38.md)

<br>

### Technical analysis

We have verified that the payload increases the bucket capacity of the CCIP facilitator on Arbitrum from 1M GHO to 2.5M GHO and that the bridgeLimit is also increased from 1M GHO to 2M GHO on Ethereum side.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


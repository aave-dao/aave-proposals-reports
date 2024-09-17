# Proposal 167. Gho Borrow Rate Update September 2024.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=167](https://vote.onaave.com/proposal/?proposalId=167)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-stewards-gho-parameter-adjustments/17289/32](https://governance.aave.com/t/arfc-gho-stewards-gho-parameter-adjustments/17289/32)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x0bCb020D88883a671a91c7775Bd898A52cF2F01D#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal decreases GHO base variable borrow rate on Aave-V3-Ethereum from 5% to 4.25% to enhance its competitiveness in the current market conditions.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x089230ae4e10894f2eee9dafeb556ea2b3ce32e397f89a793d825f7d72cbdffc](https://etherscan.io/tx/0x089230ae4e10894f2eee9dafeb556ea2b3ce32e397f89a793d825f7d72cbdffc)

```
- proposalId: 167
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x8f48e7201b581c5b1398cc1fc113ad7441e1c349cb80d29b84034a6dc039d2c6
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
      "payloadId": "174" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x8f48e7201b581c5b1398cc1fc113ad7441e1c349cb80d29b84034a6dc039d2c6" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/167.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/167.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/174.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/174.md)

<br>

### Technical analysis

We have verified that the payload decreases Gho base variable borrow rate on Aave-V3-Ethereum from 5% to 4.25%.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

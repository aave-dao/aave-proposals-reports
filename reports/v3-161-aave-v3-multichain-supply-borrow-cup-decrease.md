# Proposal 161. Decrease Supply and Borrow Caps on Aave V3.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=161](https://vote.onaave.com/proposal/?proposalId=161)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-decrease-supply-and-borrow-caps-on-aave-v3-08-28-2024/18793](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-decrease-supply-and-borrow-caps-on-aave-v3-08-28-2024/18793)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xBbb09Ad48364E1E7aA55B6c2b21644f158a6bA9C#code#F1#L1)
* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xC0812D60C47e5485baf1Bc1C51bC9962D68C03f9#code#F1#L1)
* BNB - [proposal payloads](https://bscscan.com/address/0x10335D5af1180545A739c994c525c42De9322E16#code#F1#L1)



<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal decreases the supply and borrow cups on Aave V3 deployments.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xf8e0134eda6d61ed9fe06493921a23b6519f90eefb46abad78c40a0a85510850](https://etherscan.io/tx/0xf8e0134eda6d61ed9fe06493921a23b6519f90eefb46abad78c40a0a85510850)

```
- proposalId: 161
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xd11e1cdada4dcc3b4da302aefd45121753a2ef053a7f835157a3b3c831e07e05
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
      "payloadId": "169" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "48" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "21" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xd11e1cdada4dcc3b4da302aefd45121753a2ef053a7f835157a3b3c831e07e05" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/161.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/161.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/169.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/169.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/48.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/48.md)

* BNB - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/21.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/21.md)


<br>

### Technical analysis

We have confirmed that the payload successfully adjusts the supply and borrow cups for the specified assets across the specified Aave deployments.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

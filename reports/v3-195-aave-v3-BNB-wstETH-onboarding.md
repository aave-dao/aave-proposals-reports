# Proposal 195. Onboard wstETH to BNB Chain

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=195](https://vote.onaave.com/proposal/?proposalId=195)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-wsteth-to-aave-v3-on-bnb-chain/18501/11](https://governance.aave.com/t/arfc-onboard-wsteth-to-aave-v3-on-bnb-chain/18501/11)

<br>

### Payloads

* BNB Chain - [proposal payloads](https://bscscan.com/address/0x07f29EdBcB0A4734646cB2A30d4dDA9975E16eAD#code#F1#L24)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboards wstETH to the Aave v3 BNB Chain Instance. Configures new emodes for wstETH, wETH. 
<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3a393f0e74ef2049b1f81902905a1107cca2c39483e310c3c4f5031438986459](https://etherscan.io/tx/0x3a393f0e74ef2049b1f81902905a1107cca2c39483e310c3c4f5031438986459)

```
- proposalId: 195
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xee18ffb7b418b0c4d36d9ffb0d5d8280c65e2d69df615af8c6aec49687e42716
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "26" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xee18ffb7b418b0c4d36d9ffb0d5d8280c65e2d69df615af8c6aec49687e42716" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/195.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/191.md)

**Payload reports**

* BNB Chain - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/26.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/26.md)

<br>

### Technical analysis

We have verified that the payloads lists wstETH on BNB Pool with the parameters mentioned in the IPFS. The emode for the specified assets has been configured correctly and the emission manager configured properly.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


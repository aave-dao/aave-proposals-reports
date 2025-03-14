# Proposal 269. Aave V3.3 Celo Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=269)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-deployment-on-celo/17636)

### Payloads

* Celo - [proposal payloads](https://celoscan.io/address/0xb7611d8A3Bba119ACb6E97614e1022dC3Fde4298#code)


## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets



### Context
This proposal allows the Aave governance to activate the Aave V3 Celo pool (3.3) by completing all the initial setup and listing CELO, USDC, USDT, cUSD, cEUR as suggested by the risk service providers engaged with the DAO on the governance forum.


### Proposal Creation
Transaction: [0xc1ebcf98adf5cfb49d069ca00c9c62cf9ad0adc96bfd7a9e0c23b74e76df70df](https://etherscan.io/tx/0xc1ebcf98adf5cfb49d069ca00c9c62cf9ad0adc96bfd7a9e0c23b74e76df70df)
- `proposalId`: 269
- `creator`: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- `accessLevel`: 1
- `ipfsHash`: 0x96ec601543fb7a40dfd26d454be6e041651a761593d8498c4e347c2e8cc4e6f2

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "42220", 
      "accessLevel": "1", 
      "payloadsController": "0xE48E10834C04E394A04BF22a565D063D40b9FA42", 
      "payloadId": "1" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x96ec601543fb7a40dfd26d454be6e041651a761593d8498c4e347c2e8cc4e6f2" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/269.md)

**Payload Reports**

* Celo - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42220/0xE48E10834C04E394A04BF22a565D063D40b9FA42/1_forge.md)


### Technical Analysis
We have verified the risk parameters are configured to the correct amounts. The price feeds are correct. The supply to the pool is correct.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
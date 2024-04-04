# Proposal 63. Funding Update (Part B).

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=63](https://vote.onaave.com/proposal/?proposalId=63)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-funding-update/16675/4](https://governance.aave.com/t/arfc-funding-update/16675/4)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xdE406AF1cc0595aB4e3a28C3b9C2e7edE0Fb12BE#code#F1#L129)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is a collection of treasury management actions that mainly aim to consolidate the ecosystem holdings in gho and preparing treasury for upcoming expected expenses. This is the second stage the proceed AIP 44.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x960c614e926627814bd9703fc494376f7bd1f905f9109cbde5ebd83825f7145d](https://etherscan.io/tx/0x960c614e926627814bd9703fc494376f7bd1f905f9109cbde5ebd83825f7145d)

```
- proposalId: 63
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x701e50da130aa5a24c11341bd14d57ab58e61d3691d55bd2edc849c2be9b5170
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
      "payloadId": "90" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x701e50da130aa5a24c11341bd14d57ab58e61d3691d55bd2edc849c2be9b5170" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/63.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/63.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/90.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/90.md)

<br>

### Technical analysis

We have verified that the payload is executing the following actions:

1. All the treasury's direct holdings of CRV and BAL underlying were withdrawn and transferred to the ALC SAFE wallet.

2. All the treasury's direct holdings of DAI underlying were deposited in pool V3.

3. All the treasury's direct holdings of ETH underlying were wrapped into WETH and then deposited in pool V3.

4. Treasury holdings withdrawn and transferred to swapper, sending a swap request to gho:
  1. 350 DPI were withdrawn from treasury and sent to the swapper
  2. 640k aUSDC were withdrawn from pool V2 and sent to swapper

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

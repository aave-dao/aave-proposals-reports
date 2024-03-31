# Proposal 61. Activate Gho Stewards.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=61](https://vote.onaave.com/proposal/?proposalId=61)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-stewards-borrow-rate-update/16956](https://governance.aave.com/t/arfc-gho-stewards-borrow-rate-update/16956)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x487321d27928294124Abd0Beb48F6bB7F60c8c66#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal sets the gho steward V2 as a permissioned contract that can change configurations of the gho token and gsms.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x83a8768c6399d4c93fff30a3148d54cbc5851bfe9eeeb3c374c559af16f7b81e](https://etherscan.io/tx/0x83a8768c6399d4c93fff30a3148d54cbc5851bfe9eeeb3c374c559af16f7b81e)

```
- proposalId: 61
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x111fca5019e0bc411dc4bfa36167ad7d88c57c9ddbffb202fb1568e16dd06570
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
      "payloadId": "88" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x111fca5019e0bc411dc4bfa36167ad7d88c57c9ddbffb202fb1568e16dd06570" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/61.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/61.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/88.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/88.md)

<br>

### Technical analysis

We have verified that the payload is granting the new gho steward the following roles:
- Pool Admin of the Aave V3 pool.
- Bucket Manager of the Gho token.
- Configurator of the USDC and USDT GSM.

In addition, all the existing facilitators were whitelisted within the steward contract.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

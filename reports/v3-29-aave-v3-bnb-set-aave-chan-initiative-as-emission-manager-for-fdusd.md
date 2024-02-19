# Proposal 29. Set Aave Chan Initiative as Emission Manager for fdUSD on BNB Chain Aave V3.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=29](https://vote.onaave.com/proposal/?proposalId=29)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-set-aave-chan-initiative-as-emission-manager-for-fdusd-on-bnb-chain-aave-v3/16558](https://governance.aave.com/t/arfc-set-aave-chan-initiative-as-emission-manager-for-fdusd-on-bnb-chain-aave-v3/16558)

<br>

### Payloads

* BNB V3 - [proposal payloads](https://bscscan.com/address/0xa7E28745cF5366B621e03C41dD6E8C6eF6E5D646#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal registers the Aave Chan Initiative wallet as Emission Manager for fdUSD on BNB Chain Aave V3 in order to promote growth and expand the user base of Aave on the BNB Chain.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8b16bc6b691d79987a029ae84397517a1d5061086de7e31ef5ae89bcb6e5b576](https://etherscan.io/tx/0x8b16bc6b691d79987a029ae84397517a1d5061086de7e31ef5ae89bcb6e5b576)

```
- proposalId: 29
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x9312b025853064cf395dbf32add123bdd419b0216457d59fd3941db89890c814
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "56",
      "accessLevel": 1,
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
      "payloadId": "4"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x9312b025853064cf395dbf32add123bdd419b0216457d59fd3941db89890c814"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/29.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/29.md)

**Payload reports**

* BNB V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/4.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/4.md)
  
<br>

### Technical analysis

We have verified that the payload registers the Aave Chan Initiative wallet as Emission Manager for fdUSD on BNB Chain Aave V3.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

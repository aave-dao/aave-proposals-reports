# Proposal 24. Reserve Factor Updates (Jan 31, 2024).

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=24](https://vote.onaave.com/proposal/?proposalId=24)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937)

<br>

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0xf7581bcedd5Ee02C8812cf721452d2314ff008e1#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the reserve factors of the following assets on Aave-V2-Polygon by 5% up to 99%: DAI, USDC, USDT, wETH, MATIC, in order to reduce deposit yield on Polygon v2 encouraging people to migrate from Polygon v2 to v3.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd2fdca8b0c6e853bd24a980c2ddd891e4e1814d82fdfd48a5a13c24dd3193c9d](https://etherscan.io/tx/0xd2fdca8b0c6e853bd24a980c2ddd891e4e1814d82fdfd48a5a13c24dd3193c9d)

```
- proposalId: 24
- creator: 0x2cc1ade245020fc5aae66ad443e1f66e01c54df1
- accessLevel: 1
- ipfsHash: 0xee81375a113564e990021db582f787e045b68d85f146e4a6dc6def36dd06ace9
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "137",
      "accessLevel": 1,
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
      "payloadId": "34"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xee81375a113564e990021db582f787e045b68d85f146e4a6dc6def36dd06ace9"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/24.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/24.md)

**Payload reports**

* Polygon V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/34.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/34.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor of the following tokens:

DAI: 71%

USDC: 73%

USDT: 72%

wETH: 95%

MATIC: 91%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

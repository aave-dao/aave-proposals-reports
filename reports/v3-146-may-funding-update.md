# Proposal 146. May Funding Update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=146](https://vote.onaave.com/proposal/?proposalId=146)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-may-funding-update/17768](https://governance.aave.com/t/arfc-may-funding-update/17768)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x2875727803B66688A7B6103A6b947CA9AE1f13d9#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x8d33D1f1b15ABfb2Ab462B57bC44FD2599a3a11c#code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xD1b75626c95dBf0e591C83e988452467e6641357#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xa2A221e456a1b95eC5baA7E1e8Ee39fb8Cf61d62#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is May's funding update which includes financial actions in order to enhance the financial sustainability of the DAO.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xbd37c8d8031c5c83af38601116240f9561a577fad36f7053ef51a49cca85ee06](https://etherscan.io/tx/0xbd37c8d8031c5c83af38601116240f9561a577fad36f7053ef51a49cca85ee06)

```
- proposalId: 146
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0x94033131f9158cfc102cbc37a63245c05b9c9c475bfe22b3ecdc288f1a637c4d
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
      "payloadId": "158"
    },
    {
      "chain": "137",
      "accessLevel": "1",
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
      "payloadId": "76"
    },
    {
      "chain": "10",
      "accessLevel": "1",
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
      "payloadId": "43"
    },
    {
      "chain": "42161",
      "accessLevel": "1",
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
      "payloadId": "45"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x94033131f9158cfc102cbc37a63245c05b9c9c475bfe22b3ecdc288f1a637c4d"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/146.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/146.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/158.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/158.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/76.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/76.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/43.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/43.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/45.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/45.md)

<br>

### Technical analysis

We have verified that the payloads do the financial actions which are declared in the IPFS, except some inconsistencies with the amount of Atokens which comes from using balanceOf instead of scaledBalanceOf, but no effect will be caused by this.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum except the amounts of aEthUSDT, aEthUSDC and the note regarding the Atokens above.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


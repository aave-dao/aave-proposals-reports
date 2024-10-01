# Proposal 175. Onboard USDS on Aave V3 Ethereum Main and Lido Instance.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=175](https://vote.onaave.com/proposal/?proposalId=175)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-usds-and-susds-to-aave-v3/18987/9](https://governance.aave.com/t/arfc-onboard-usds-and-susds-to-aave-v3/18987/9)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xAC088db10BCEBd1c4199f27a79A5d9755A546140#code#F1#L1)

* EthereumLido - [proposal payloads](https://etherscan.io/address/0x87Bcde5883012293cD673e874dbcfb6b6F21cfBA#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboards USDS, the rebranded DAI token to Aave v3 Ethereum Main and Lido Pool in order to to maintain continuity for users who have relied on DAI while embracing the evolution of these assets under the Sky brand.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x686bd0613d340672235b3e47c0cda56a21f3f151e612c31c0b9b2e128537b1e9](https://etherscan.io/tx/0x686bd0613d340672235b3e47c0cda56a21f3f151e612c31c0b9b2e128537b1e9)

```
- proposalId: 175
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0xe2efa3b07ac0333e5b8f6b57377a4ace8d43add290b780ac9924d6131ae797f7
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
      "payloadId": "183"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xe2efa3b07ac0333e5b8f6b57377a4ace8d43add290b780ac9924d6131ae797f7"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/175.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/175.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/183.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/183.md)

<br>

### Technical analysis

We have verified that the payloads lists USDS on both Ethereum Main and Lido Pool with the parameters mentioned in the IPFS.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


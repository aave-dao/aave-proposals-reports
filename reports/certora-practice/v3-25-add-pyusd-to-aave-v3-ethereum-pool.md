# Proposal 25. Add PYUSD to Aave v3 Ethereum Pool.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=25](https://vote.onaave.com/proposal/?proposalId=25)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-pyusd-to-aave-v3-ethereum-market/16218](https://governance.aave.com/t/arfc-add-pyusd-to-aave-v3-ethereum-market/16218)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xF794a27313d7C5Ce45E572891243F8c604910D0e#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: listing new assets

<br>

### Context

This proposal aims to onboard the PYUSD stable coin on the Aave-v3 protocol on Ethereum network.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8cbdf6a3055bfa84cd6d4adcf291b56183d6f6a9d85f4db865c255c5977d8154](https://etherscan.io/tx/0x8cbdf6a3055bfa84cd6d4adcf291b56183d6f6a9d85f4db865c255c5977d8154)

```
- proposalId: 25
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xe51a388c30d2cfac5e7e2a68d626cd21ea90e8b863e4e60dc31aa10725fc7a87
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
      "payloadId": "60"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xe51a388c30d2cfac5e7e2a68d626cd21ea90e8b863e4e60dc31aa10725fc7a87"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/25.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/25.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/60.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/60.md)

<br>

### Technical analysis

We have verified that the payload executing the following financial actions:

- listing the PYUSD stable coin with the parameters according to the specified table in the IPFS. 

- supplying 1 PYUSD to the Ethereum collector.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

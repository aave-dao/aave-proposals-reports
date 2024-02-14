# Proposal 14. Treasury Management - GSM Funding & RWA Strategy Preparations (Part 1), Frontier Staking as a Service

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=14](https://vote.onaave.com/proposal/?proposalId=14)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-treasury-management-gsm-funding-rwa-strategy-preparations/16128](https://governance.aave.com/t/arfc-treasury-management-gsm-funding-rwa-strategy-preparations/16128)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x7cAAf036c24e38eeA0688d2eD52A756Df83037fB#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x5E6ac2EEd9b13C4D093a281E78feda6bF4f6a8b5#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal bundles three financial arrangements:

- prepares the ground for the GSM and RWA strategy with Centirfuge activision by bridging assets from polygon to ethereum

- nullifies the allowances of three addresses for the ethereum collector

- withdrawing 128 WETH from v2 to a safe as preparation for the "Frontier" initiative.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x852847fcf90960c14e8dbe6f0916a712e1976efb6482bbbc6f3c666e6dd59b2c](https://etherscan.io/tx/0x852847fcf90960c14e8dbe6f0916a712e1976efb6482bbbc6f3c666e6dd59b2c)

```
- proposalId: 14
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x36664a88ec779d778e529d1175762ae8b062bcedc553c07936e158255ad31700
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
      "payloadId": "52"
    },
    {
      "chain": "137",
      "accessLevel": 1,
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
      "payloadId": "30"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x36664a88ec779d778e529d1175762ae8b062bcedc553c07936e158255ad31700"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/14.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/14.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/52.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/52.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/30.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/30.md)

<br>

### Technical analysis

We have verified that the payloads executing the following financial actions:

- all of aUSDC, aUSDT, aDAI from polygon-v2 and all aUSDC, aUSDT and 1M aDAI from polygon-v3 were bridged to ethereum apart from 10 units of each token

- all three addresses on ethereum were revoked any allowance from the collector according to the specified table in the IPFS.

- 128 WETH were withdrawn from collector-v2 converted to ETH and sent to the specified safe address.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

# Proposal 186. Chaos Labs &lt;&gt; Aave Risk Management Service Renewal.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=186](https://vote.onaave.com/proposal/?proposalId=186)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-aave-risk-management-service-renewal/19306](https://governance.aave.com/t/arfc-chaos-labs-aave-risk-management-service-renewal/19306)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xE21d4e375Cd138812f4a4b6249B34234b92f2094#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:bank: payment stream

<br>

### Context

This proposal is the renewal of the risk service provider - Chaos Labs for a duration of 12 months since their last engagement, for the price of 2,000,000$ - 1,000,000$ in GHO, 1,000,000$ in aEthUSDT.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xad6abb2b749bfe26625716d3c4372b0751112729e2c92f7cb73094e9eda6a396](https://etherscan.io/tx/0xad6abb2b749bfe26625716d3c4372b0751112729e2c92f7cb73094e9eda6a396)

```
- proposalId: 186
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0x70d848896b97f549376d1197f43a69c58246fec57b5314c76dc1749a5f1759b3
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
      "payloadId": "194"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x70d848896b97f549376d1197f43a69c58246fec57b5314c76dc1749a5f1759b3"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/186.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/186.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/194.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/194.md)

<br>

### Technical analysis

We have verified that the payload creates 2 streams of 1,000,000 GHO and 1,000,000 aEthUSDT for a duration of 365 days (12 months) for the address provided by Chaos Labs.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


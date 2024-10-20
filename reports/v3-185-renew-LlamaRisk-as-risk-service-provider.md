# Proposal 185. Renew LlamaRisk as Risk Service Provider.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=185](https://vote.onaave.com/proposal/?proposalId=185)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-renew-llamarisk-as-risk-service-provider/19277](https://governance.aave.com/t/arfc-renew-llamarisk-as-risk-service-provider/19277)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9ECAE4b686BF3D6Ce72015D4C29B2B86Cc34f0eD#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:bank: payment stream

<br>

### Context

This proposal is the renewal of the risk service provider - LlamaRisk for a duration of 6 months since their last engagement, for the price of 400,000$ in GHO.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xbb1307e331430b74dcc9f245a92dfb1c9be2a9ce2616cdc3d1e526f8021373eb](https://etherscan.io/tx/0xbb1307e331430b74dcc9f245a92dfb1c9be2a9ce2616cdc3d1e526f8021373eb)

```
- proposalId: 185
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0xf0812faba2ea8655fa8db894c5b06515dea31a90b702f7e606169a025648abdd
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
      "payloadId": "193"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xf0812faba2ea8655fa8db894c5b06515dea31a90b702f7e606169a025648abdd"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/185.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/185.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/193.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/193.md)

<br>

### Technical analysis

We have verified that the payload creates a stream of 400,000 GHO for a duration of 182 days (6 months) for the address provided by LlamaRisk.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


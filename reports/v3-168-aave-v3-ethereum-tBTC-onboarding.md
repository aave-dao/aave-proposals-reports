# Proposal 168. Aave v3 Ethereum tBTC Onboarding.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=168](https://vote.onaave.com/proposal/?proposalId=168)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-tbtc-to-aave-v3-on-ethereum-arbitrum-and-optimism/17686/12](https://governance.aave.com/t/arfc-onboard-tbtc-to-aave-v3-on-ethereum-arbitrum-and-optimism/17686/12)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x785c44862ed5026Bbe4DcD1f7103b1D30cBf7cBa#code#F1#L37)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

The proposal aims to onboard Threshold Network’s tBTC, to the Aave v3 protocol on Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xea7d8a468ba6501eb80c0c6d6ef1f0e0e84413c90347d3c201c43d7174752c69](https://etherscan.io/tx/0xea7d8a468ba6501eb80c0c6d6ef1f0e0e84413c90347d3c201c43d7174752c69)

```
- proposalId: 169
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x81a5fdd7fab7ee5b45231af1b8934dea3a93ce530575bcce16dc7bb74691b6c7
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
      "payloadId": "175" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xc6a9b3c0acd8996082cfea92cb8b8bd150f68425ad355909539311f710b8c40f" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/168.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/168.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/175.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/175.md)

<br>

### Technical analysis

We have verified that the payload correctly sets up the parameters for the asset. We have verified that the payload supplies the asset to the pool to avoid a first deposit attack. The use of the BTC/USD price feed (instead of tBTC/USD) is supported by the DAO as specified in the forum.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

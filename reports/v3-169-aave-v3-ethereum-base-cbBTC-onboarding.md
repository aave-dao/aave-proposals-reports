# Proposal 169. Aave v3 Ethereum and Base cbBTC Onboarding.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=169](https://vote.onaave.com/proposal/?proposalId=169)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-cbbtc-to-aave-v3-on-base-and-mainnet/18988/14](https://governance.aave.com/t/arfc-onboard-cbbtc-to-aave-v3-on-base-and-mainnet/18988/14)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9edaC3Ce0Fc919f792d3B72D767d22FD382Faf21#code#F1#L33)

* Base - [proposal payloads](https://basescan.org/address/0x8C97eC66De2A0167fF1048E4D9A77E90067c98eb#code#F1#L37)


<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

The proposal aims to onboard Coinbase’s cbBTC, to the Aave v3 protocol on Mainnet main instance & Base.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xdfb4b958807e0cb3a360d93eee97d466a93e35a3e593f4ff25b4b4f1767813e3](https://etherscan.io/tx/0xdfb4b958807e0cb3a360d93eee97d466a93e35a3e593f4ff25b4b4f1767813e3)

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
      "payloadId": "176" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "36" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x81a5fdd7fab7ee5b45231af1b8934dea3a93ce530575bcce16dc7bb74691b6c7" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/169.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/169.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/176.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/176.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/36.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/36.md)

<br>

### Technical analysis

We have verified that the payload correctly sets up the parameters for the asset. We have verified that the payload supplies the asset to the pool to avoid a first deposit attack. The use of the BTC/USD price feed (instead of cbBTC/USD) is supported by the DAO as specified in the forum.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

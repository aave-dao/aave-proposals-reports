# Proposal 105. Chaos Labs Ethereum V2 LT Reductions.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=105](https://vote.onaave.com/proposal/?proposalId=105)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-ethereum-v2-lt-reductions-05-06-2024/17598](https://governance.aave.com/t/arfc-chaos-labs-ethereum-v2-lt-reductions-05-06-2024/17598)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xDc38DBcAE6Be78DA84972afB07825726615cbd23#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal reduces the liquidation thresholds of ZRX, LINK which are frozen assets on Aave-V2-Ethereum and in order to encourage users to migrate from v2 to v3. 

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x441c941bbbf59e21701d0a6c5d36f8b6dbb9602e9a829daf4a157acb1bb5620c](https://etherscan.io/tx/0x441c941bbbf59e21701d0a6c5d36f8b6dbb9602e9a829daf4a157acb1bb5620c)

```
- proposalId: 105
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x6c9644b3c657187c2d9d8632de3eaf2ab1d689f328d18d6bc83a65bed945d3d0
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
      "payloadId": "127" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x6c9644b3c657187c2d9d8632de3eaf2ab1d689f328d18d6bc83a65bed945d3d0" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/105.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/105.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/127.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/127.md)

<br>

### Technical analysis

We have verified that the payload reduces the liquidation thresholds of the following tokens to the following values:

- Ethereum V2:

    LINK: 65.00%

    ZRX: 0.01%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

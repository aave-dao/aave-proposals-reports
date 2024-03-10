# Proposal 44. Funding Update

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=44](https://vote.onaave.com/proposal/?proposalId=44)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-funding-update/16675](https://governance.aave.com/t/arfc-funding-update/16675)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xE94d276b7a109b71Dd9f1C032AB089F861557d2F#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xcd04Bbe5bBE9f68Aedf917962e1783D5f4Cb0d8F#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is a collection of treasury management actions that mainly aim to consolidate the ecosystem holdings in gho and preparing treasury for upcoming expected expenses.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1a338482eda6083f05c70a9cf9db45971cfc7667b5b8f79c3e8d8b96466de6ea](https://etherscan.io/tx/0x1a338482eda6083f05c70a9cf9db45971cfc7667b5b8f79c3e8d8b96466de6ea)

```
- proposalId: 44
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0x4297b59c6e7926b8507d06c9541d975a7fad0f6e16bd28986262431a342b828e
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
      "payloadId": "73" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "40" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x4297b59c6e7926b8507d06c9541d975a7fad0f6e16bd28986262431a342b828e" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/44.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/44.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/73.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/73.md)

* Polygon V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/40.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/40.md)

<br>

### Technical analysis

We have verified that the payloads are executing the following actions:

On polygon, all the the ecosystem holdings of the assets WETH, DAI, BAL and CRV are withdrawn from the collector to the benefit of the bridge, and then bridge the assets to Ethereum.

On Ethereum, the following actions were made:

1. All treasury's aWBTC, aWETH holdings + 300k of aUSDC were withdrawn from the V2 pool and deposited on behalf of the collector in the V3 pool.

2. All treasury holdings of CRV and BAL, including direct holding of underlying and aTokens on V2 and V3 pools, were withdrawn and transferred to the ALC SAFE wallet.

3. Treasury holdings withdrawn and transferred to swapper, sending a swap request to gho:
  1. All holdings of LUSD - as underlying or deposited to either pool V2 or V3 were withdrawn and sent to the swapper
  2. All the DAI, FRAX and DPI were withdrawn from pool V2 and sent to the swapper
  3. 1.25M USDC were withdrawn from pool V3 and sent to swapper
  4. All the current holdings of USDT underlying + an amount complimenting to 1.5M USDT was withdrawn from the pool V3. In addition, 200k of USDT were withdrawn from pool V2. Bringing a total of 1.7M USDT sent from treasury holdings to the swapper.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

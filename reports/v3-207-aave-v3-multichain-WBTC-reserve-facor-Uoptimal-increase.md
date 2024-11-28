# Proposal 207. WBTC Reserve Factor and UOptimal Increase


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=207](https://vote.onaave.com/proposal/?proposalId=207)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-wbtc-reserve-factor-and-uoptimal-increase-10-25-24/19596](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-wbtc-reserve-factor-and-uoptimal-increase-10-25-24/19596)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x30636F60a18521c155e5AB61F85b18a92Ce49945#code)

* Polygon - [proposal payloads](https://etherscan.io/address/0xdda76EF1c1Fd3747c8093BB331B61CD4F7362C81#code)

* Optimism - [proposal payloads](https://etherscan.io/address/0x705B90d858dda82B8094B5f5864A21c36CC2020A#code)

* Arbitrum - [proposal payloads](https://etherscan.io/address/0x650e698aB9204430335Cc9d4059646f21c532dBB#code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal by Chaos Labs recommends increasing WBTC’s Reserve Factor from 20% to 50% and UOptimal from 45% to 80% across all Aave V3 instances. The changes aim to boost DAO revenue and accommodate growing demand from yield-bearing BTC collateral assets, driven by the launch of Liquid E-Modes and staked BTC’s popularity. WBTC’s historical use as collateral, with minimal sensitivity to supply rates, supports these adjustments, ensuring protocol stability and attractiveness. These updates align Aave’s parameters with market dynamics while preparing for increased borrowing demand.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6b58930abe94070312fd8b9283fa7f363d9d9d471a31aa9998be33b3bbcacaf3](https://etherscan.io/tx/0x6b58930abe94070312fd8b9283fa7f363d9d9d471a31aa9998be33b3bbcacaf3)

```
- proposalId: 207
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x979ccf480bc88243e4cca46bce6a65766eb6cc93d189e0dd911ac3c54ed0b1be
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
      "payloadId": "212" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "89" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "57" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "61" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x979ccf480bc88243e4cca46bce6a65766eb6cc93d189e0dd911ac3c54ed0b1be" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/207.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/207.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/212.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/212.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/89.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/89.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/57.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/57.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/61.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/61.md)


<br>

### Technical analysis

We have verified that the contract implements the proposed changes correctly, setting the Reserve Factor to 50% and UOptimal to 80% as intended. The WBTC_UNDERLYING token address is accurately referenced across all Aave V3 instances, and the Seatbelt report confirms the integrity of the parameter updates with no unintended modifications. This ensures the proposal aligns with its stated goals and is ready for execution.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


# Proposal 39. Set Liquidity Observation Labs as Emission manager for wstETH on V3 markets

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=39](https://vote.onaave.com/proposal/?proposalId=39)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-set-liquidity-observation-labs-as-emission-manager-for-wsteth-on-v3-markets/16479](https://governance.aave.com/t/arfc-set-liquidity-observation-labs-as-emission-manager-for-wsteth-on-v3-markets/16479)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xDd5929b58F9557b97fF1B46B725b75089a07bA32#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x81b1D1B293F98194b98024ED38EA4D42682BC7C7#code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x6826D5e19D1589A2f64F878d677A8c1e261Bc15B#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x1f16398Cb27c744bD87008aaEC801FC810271543#code#F1#L1)

* Base - [proposal payloads](https://basescan.org/address/0xeB0b55cE74a8B4A614DD2163E35Eaeb4739f0758#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal sets Lido Liquidity Observation Labs' as the incentives emission manager for wstETH on multiple chains to promote growth of the protocol.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9b989071bc1c6d5754922e9e61f052c5fb490a161a5e60106db45b10ac1854db](https://etherscan.io/tx/0x9b989071bc1c6d5754922e9e61f052c5fb490a161a5e60106db45b10ac1854db)

```
- proposalId: 39
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x6f3e2a38b68d225055ea1f4d82ac73ef779d27eb11834fdbbfcd0a8652971289
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
      "payloadId": "69"
    },
    {
      "chain": "137",
      "accessLevel": 1,
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
      "payloadId": "38"
    },
    {
      "chain": "10",
      "accessLevel": 1,
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
      "payloadId": "13"
    },
    {
      "chain": "42161",
      "accessLevel": 1,
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
      "payloadId": "12"
    },
    {
      "chain": "8453",
      "accessLevel": 1,
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
      "payloadId": "7"
    }
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x6f3e2a38b68d225055ea1f4d82ac73ef779d27eb11834fdbbfcd0a8652971289"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/39.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/39.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/69.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/69.md)

* Polygon V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/38.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/38.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/13.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/13.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/12.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/12.md)

* Base V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/7.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/7.md)

<br>

### Technical analysis

We have verified that the payloads sets the declared address, `0xC18F11735C6a1941431cCC5BcF13AF0a052A5022`, as an emission manager of wstETH on the aforementioned chains.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

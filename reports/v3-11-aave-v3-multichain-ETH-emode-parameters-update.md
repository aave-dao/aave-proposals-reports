# V3. Proposal 11. Aave v3 Ethereum, Optimism, Arbitrum - ETH e-mode parameters update

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=11](https://vote.onaave.com/proposal/?proposalId=11)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-update-steth-and-weth-risk-params-on-aave-v3-ethereum-optimism-and-arbitrum/16168/7](https://governance.aave.com/t/arfc-update-steth-and-weth-risk-params-on-aave-v3-ethereum-optimism-and-arbitrum/16168/7)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates risk parameters and rate strategies configuration for ETH e-mode on Aave v3 Ethereum, Optimism and Arbitrum. Additionally, the Optimal Point of the WETH rate strategy is updated in those Aave v3 instances.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6a9365f8359afbbf91a7916bc7b0d141db18422c934fcd3f531aedd64ac59e01](https://etherscan.io/tx/0x6a9365f8359afbbf91a7916bc7b0d141db18422c934fcd3f531aedd64ac59e01)


```
- proposalId: 11
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x2fa324a635a80a4f64b8636199440b6ef8687135aa81ccf396570eb8aecc7bed
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdabad81af85554e9ae636395611c58f7ec1aaec5",
      "payloadId": "50"
    },
    {
      "chain": "10",
      "accessLevel": 1,
      "payloadsController": "0x0e1a3af1f9cc76a62ed31ededca291e63632e7c4",
      "payloadId": "10"
    },
    {
      "chain": "42161",
      "accessLevel": 1,
      "payloadsController": "0x89644ca1bb8064760312ae4f03ea41b05da3637c",
      "payloadId": "9"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0x2fa324a635a80a4f64b8636199440b6ef8687135aa81ccf396570eb8aecc7bed"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/11.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/11.md)

**Payloads report**

**Ethereum**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/50.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/50.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/50_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/50_forge.md)

<br>

**Optimism**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/10.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/10.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/10_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/10_forge.md)

<br>

**Arbitrum**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/9.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/9.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/9_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/9_forge.md)

<br>

<br>

### Technical analysis

The proposal is composed by 3 payloads, one for each network. We have verified they do the following changes.

**[Ethereum](https://etherscan.io/address/0x983921EFA9859880d8dc66c90BE93f18C02B3A1A#code#F1#L17)**

- ETH e-mode LTV: 90% -> **93%**
- ETH e-mode LT: 93% -> **95%**
- WETH rate strategy optimal point: 80% -> **90%**

<br>

**[Optimism](https://optimistic.etherscan.io/address/0x443d2441F3b45167C4ECDDa9985DF8dCFAad6e08#code#F1#L17)**

- ETH e-mode LTV: 90% -> **93%**
- ETH e-mode LT: 93% -> **95%**
- WETH rate strategy optimal point: 80% -> **90%**

<br>

**[Arbitrum](https://arbiscan.io/address/0x641Bb6A9a092EDBaE407373e2B563400617229d2#code#F1#L16)**

- ETH e-mode LTV: 90% -> **93%**
- ETH e-mode LT: 93% -> **95%**
- ETH e-mode LB: 2% -> **1%**
- WETH rate strategy optimal point: 80% -> **90%**

<br>

<br>

Even if in the forum there is some discussion and feedback from risk providers, the payloads are consistent with the final decision on Snapshot

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

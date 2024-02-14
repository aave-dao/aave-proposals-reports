# Proposal 11. Update ETH EMode and WETH Risk Params on Aave v3 Ethereum, Optimism and Arbitrum

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=11](https://vote.onaave.com/proposal/?proposalId=11)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-update-steth-and-weth-risk-params-on-aave-v3-ethereum-optimism-and-arbitrum/16168](https://governance.aave.com/t/arfc-update-steth-and-weth-risk-params-on-aave-v3-ethereum-optimism-and-arbitrum/16168)

<br>

### Payloads

* Ethereum V3 - [https://etherscan.io/address/0x983921EFA9859880d8dc66c90BE93f18C02B3A1A#code#F1#L23](https://etherscan.io/address/0x983921EFA9859880d8dc66c90BE93f18C02B3A1A#code#F1#L23)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/9.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/9.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/10.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/10.md)
<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal suggests an optimization of the e-mode risk parameters of ETH correlated assets on Ethereum mainnet, Arbitrum and Optimism, in order to get better market efficiency.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6a9365f8359afbbf91a7916bc7b0d141db18422c934fcd3f531aedd64ac59e01](https://etherscan.io/tx/0x6a9365f8359afbbf91a7916bc7b0d141db18422c934fcd3f531aedd64ac59e01)

```
- proposalId: 11
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x2fa324a635a80a4f64b8636199440b6ef8687135aa81ccf396570eb8aecc7bed
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
      "payloadId": "50"
    },
    {
      "chain": "10",
      "accessLevel": 1,
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
      "payloadId": "10"
    },
    {
      "chain": "42161",
      "accessLevel": 1,
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
      "payloadId": "9"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x2fa324a635a80a4f64b8636199440b6ef8687135aa81ccf396570eb8aecc7bed"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/11.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/11.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/50.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/50.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/9.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/9.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/10.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/10.md)

<br>

### Technical analysis

We have verified that each of the payloads alters only the parameters specified in the IPFS, and exactly to the values that were specified.

* On Ethereum V3 WETH's general (non e-mode) optimal ratio were set to 90% and ETH correlated assets' (e-mode) ltv and liquidation threshold were set to 93% and 95% respectively.

* On Arbitrum V3 WETH's general (non e-mode) optimal ratio were set to 90% and ETH correlated assets' (e-mode) ltv, liquidation threshold and liquidation bonus were set to 93%, 95% and 1% respectively.

* On Optimism V3 WETH's general (non e-mode) optimal ratio were set to 90% and ETH correlated assets' (e-mode) ltv and liquidation threshold were set to 93% and 95% respectively.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

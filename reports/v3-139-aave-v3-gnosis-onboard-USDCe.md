# Proposal 139. Onboard USDC.e on Gnosis.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=139](https://vote.onaave.com/proposal/?proposalId=139)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-usdc-e-to-aave-v3-gnosis-chain/17948/3](https://governance.aave.com/t/arfc-onboard-usdc-e-to-aave-v3-gnosis-chain/17948/3)

<br>

### Payloads

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xF0221Fc5a2F825bbF6F994f30743aD5AAC66cd4E#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboards USDC.e onto Gnosis V3 in order to improve the diversity of assets on Aave and bolster liquidity within the ecosystem.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x84e6c04704b14706dadc409e325e91396ade062e6e1472033af538123ef3c109](https://etherscan.io/tx/0x84e6c04704b14706dadc409e325e91396ade062e6e1472033af538123ef3c109)

```
- proposalId: 139
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0xf419f34373957ef660343043d18871e0d104ecc83709743658edeb1d44edd6f2
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "100",
      "accessLevel": "1",
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
      "payloadId": "24"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xf419f34373957ef660343043d18871e0d104ecc83709743658edeb1d44edd6f2"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/139.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/139.md)

**Payload reports**

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/24.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/24.md)

<br>

### Technical analysis

We have verified that the payload onboards USDC.e to Gnosis V3 with the same configuration declared in the IPFS.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


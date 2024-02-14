# Proposal 20. Aave v3 Scroll Activation.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=20](https://vote.onaave.com/proposal/?proposalId=20)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-v3-deployment-on-scroll-mainnet/16126/](https://governance.aave.com/t/arfc-aave-v3-deployment-on-scroll-mainnet/16126/)

<br>

### Payloads

* Scroll - [proposal payloads](https://scrollscan.com/address/0x2B25cb729D90630395Cd3140f3460a73A41Fe5f0#code#F1#L23)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: listing new assets
:handshake: permission granting or revoking

<br>

### Context

This proposal activates the Aave-V3-Scroll pool with the following tokens: WETH, USDC, wstETH.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1a2d11e3923580a7ecd20d2a1034caa4d07eb35f6e76a1ff9d5d964fb8fdc3c4](https://etherscan.io/tx/0x1a2d11e3923580a7ecd20d2a1034caa4d07eb35f6e76a1ff9d5d964fb8fdc3c4)

```
- proposalId: 20
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xaec2b0f6a12587f140399c85050f710c50e593beac66fad4d5ea17d0901847f8
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "534352",
      "accessLevel": 1,
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
      "payloadId": "0"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xaec2b0f6a12587f140399c85050f710c50e593beac66fad4d5ea17d0901847f8"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/20.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/20.md)

**Payload reports**

* Scroll V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/0_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/0_forge.md)

<br>

### Technical analysis

We have verified that the payload executing the following actions:

- adding pool and risk admins to Scroll according to the IPFS.

- listing the WETH, USDC, wstETH tokens with the parameters according to the specified table in the IPFS. 

- supplying 0.005 WETH, wstETH and 1 USDC to the Scroll pool.

<br>

The proposal was found to be consistent with the IPFS but not with the Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

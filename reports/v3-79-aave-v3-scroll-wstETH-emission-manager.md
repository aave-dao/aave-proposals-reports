# Proposal 79. Scroll wstETH Emission Admin.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=79](https://vote.onaave.com/proposal/?proposalId=79)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-set-liquidity-observation-labs-as-emission-manager-for-wsteth-on-scroll/16813](https://governance.aave.com/t/arfc-set-liquidity-observation-labs-as-emission-manager-for-wsteth-on-scroll/16813)

<br>

### Payloads

* Scroll - [proposal payloads](https://scrollscan.com/address/0xFdF1e6d1463D34BD74313800115B300e5B3F0c13#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal propose to set an emission manager for wstETH on Scroll chain to incentivize growth of Aave v3 on the Scroll chain.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb0da2d4b172b7ac93937c83c7e74bc1a845a55cbf9caa4ab5ade240ba400651a](https://etherscan.io/tx/0xb0da2d4b172b7ac93937c83c7e74bc1a845a55cbf9caa4ab5ade240ba400651a)

```
- proposalId: 79
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x066ee4d63e49489ac41c0950213f9b95edc9c0d8a1710ffdcc35d9ade4dc7495
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "9" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x066ee4d63e49489ac41c0950213f9b95edc9c0d8a1710ffdcc35d9ade4dc7495" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/79.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/79.md)

**Payload reports**

* Scroll V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/9_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/9_forge.md)

<br>

### Technical analysis

We have verified that the payload is setting a declared Liquidity Observation Labs wallet as the emission admin of wstETH over the Scroll chain and has no further side effects.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

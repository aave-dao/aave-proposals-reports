# Proposal 140. Onboard weETH on Scroll.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=140](https://vote.onaave.com/proposal/?proposalId=140)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboarding-weeth-to-aave-v3-on-scroll/18301](https://governance.aave.com/t/arfc-onboarding-weeth-to-aave-v3-on-scroll/18301)

<br>

### Payloads

* Scroll - [proposal payloads](https://scrollscan.com/address/0x5B043e5f4C34010ADEC8a5A33A2e45F8d7586e21#code)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboards weETH onto Scroll V3 in order to improve the diversity of assets on Aave and bolster liquidity within the ecosystem.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8aaaa755d0d2c27889af5fcd5a643af1d8e54e73464cdd4c60003ac6ba34f31d](https://etherscan.io/tx/0x8aaaa755d0d2c27889af5fcd5a643af1d8e54e73464cdd4c60003ac6ba34f31d)

```
- proposalId: 140
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x653f4431fde3b935da775bcc2f0820d051c8f8342ee0cc707c1910c312d2bc66
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
      "payloadId": "16" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x653f4431fde3b935da775bcc2f0820d051c8f8342ee0cc707c1910c312d2bc66" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/140.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/140.md)

**Payload reports**

* Scroll - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/16_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/16_forge.md)

<br>

### Technical analysis

We have verified that the payload onboards weETH to Scroll V3 with the same configuration declared in the IPFS.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


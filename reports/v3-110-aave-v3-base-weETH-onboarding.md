# Proposal 110. weETH Onboarding On Base.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=110](https://vote.onaave.com/proposal/?proposalId=110)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboarding-of-weeth-to-aave-v3-on-base/17691](https://governance.aave.com/t/arfc-onboarding-of-weeth-to-aave-v3-on-base/17691)

<br>

### Payloads

* Base - [proposal payloads](https://basescan.org/address/0x0EB0410d11F7163d679E62942DD881476F9D05c4#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboards weETH on Base V3 in order to improve the diversity of assets on Aave and bolster liquidity within the ecosystem.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9d80241238a3c64b367a9d6363514aa84b977fd93196ccb42fa42070844652d9](https://etherscan.io/tx/0x9d80241238a3c64b367a9d6363514aa84b977fd93196ccb42fa42070844652d9)

```
- proposalId: 110
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x54d65f6ae8620fe173a28130e99d96315d574c380f84b37665dbc9f69232fae1
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "20" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x54d65f6ae8620fe173a28130e99d96315d574c380f84b37665dbc9f69232fae1" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/110.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/110.md)

**Payload reports**

* Base V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/20.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/20.md)

<br>

### Technical analysis

We have verified that the payload onboards weETH on Base V3 with the following parameters:

Isolation Mode - False

Borrowable - Enabled

Collateral Enabled - True

Supply Cap - 150

Borrow Cap - 30

Debt Ceiling - 0

LTV - 72.5%

LT - 75%

Liquidation Bonus - 7.5%

Liquidation Protocol Fee - 10%

Reserve Factor	- 45%

Base Variable Borrow Rate - 0%

Variable Slope 1 - 7%

Variable Slope 2 - 300%

Uoptimal - 35%

Stable Borrowing - Disabled

Stable Slope1 - 7%

Stable Slope2 - 300%

Base Stable Rate Offset - 0%

Stable Rate Excess Offset - 0%

Optimal Stable To Total Debt Ratio - 0%

Flashloanable - Enabled

Siloed Borrowing - Disabled

Borrowable in Isolation - Disabled

Oracle - 0xFc4d1d7a8FD1E6719e361e16044b460737F12C44

eMode Category - ETH_CORRELATED

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

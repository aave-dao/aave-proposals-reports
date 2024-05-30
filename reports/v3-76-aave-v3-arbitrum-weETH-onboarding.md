# Proposal 76. weETH Onboarding On Arbitrum.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=76](https://vote.onaave.com/proposal/?proposalId=76)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-weeth-to-aave-v3-on-ethereum/16758/15](https://governance.aave.com/t/arfc-onboard-weeth-to-aave-v3-on-ethereum/16758/15)

<br>

### Payloads

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xA28f92B41874Ad36A7e3177f212BC1c87497b94B#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboards weETH on Arbitrum V3 in order to improve the diversity of assets on Aave and bolster liquidity within the ecosystem.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8dc665e05507787ae5f87074de1821732b21e5e00d3bec117bb2f2364cffdef4](https://etherscan.io/tx/0x8dc665e05507787ae5f87074de1821732b21e5e00d3bec117bb2f2364cffdef4)

```
- proposalId: 76
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x78778591515790b337fcdcc2a02d49dc58e98cad614c33d61e1173bc6194729d
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "24" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x78778591515790b337fcdcc2a02d49dc58e98cad614c33d61e1173bc6194729d" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/76.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/76.md)

**Payload reports**

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/24.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/24.md)

<br>

### Technical analysis

We have verified that the payload onboards weETH on Arbitrum V3 with the following parameters:

Isolation Mode - False

Borrowable - Enabled

Collateral Enabled - True

Supply Cap - 1000

Borrow Cap - 100

Debt Ceiling - 0

LTV - 72.5%

LT - 75%

Liquidation Bonus - 7.5%

Liquidation Protocol Fee - 10%

Reserve Factor	- 15%

Base Variable Borrow Rate - 0%

Variable Slope 1 - 7%

Variable Slope 2 - 300%

Uoptimal - 45%

Stable Borrowing - Disabled

Stable Slope1 - 7%

Stable Slope2 - 300%

Base Stable Rate Offset - 2%

Stable Rate Excess Offset - 20%

Optimal Stable To Total Debt Ratio - 20%

Flashloanable - Enabled

Siloed Borrowing - Disabled

Borrowable in Isolation - Disabled

Oracle - 0x517276B5972C4Db7E88B9F76Ee500E888a2D73C3

eMode Category - ETH_CORRELATED

<br>

The proposal is consistent with the description on the governance forum, except the isolation mode on the IPFS which should be disabled.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

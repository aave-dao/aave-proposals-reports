# Proposal 104. osETH Onboarding On Ethereum.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=104](https://vote.onaave.com/proposal/?proposalId=104)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-oseth-to-aave-v3-on-ethereum/16913](https://governance.aave.com/t/arfc-onboard-oseth-to-aave-v3-on-ethereum/16913)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4f51d7cB6f62ebF9CB85D31907B99BE6e18C83Cc#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboards osETH on Ethereum V3 in order to improve the diversity of assets on Aave and bolster liquidity within the ecosystem.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x2766600b053802fc9269dd8040da47fb4e272b29cd8a3e696a6abb82474ddb7b](https://etherscan.io/tx/0x2766600b053802fc9269dd8040da47fb4e272b29cd8a3e696a6abb82474ddb7b)

```
- proposalId: 104
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x543b2ccf5ce8d534cbbfd1ed90572a717c31eccd518762f65303820dda4d285d
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
      "payloadId": "126" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x543b2ccf5ce8d534cbbfd1ed90572a717c31eccd518762f65303820dda4d285d" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/104.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/104.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/126.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/126.md)

<br>

### Technical analysis

We have verified that the payload onboards osETH on Ethereum V3 with the following parameters:

Isolation Mode - False

Borrowable - Enabled

Collateral Enabled - True

Supply Cap - 10,000

Borrow Cap - 1,000

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

Stable Slope1 - 0%

Stable Slope2 - 0%

Base Stable Rate Offset - 0%

Stable Rate Excess Offset - 0%

Optimal Stable To Total Debt Ratio - 0%

Flashloanable - Enabled

Siloed Borrowing - Disabled

Borrowable in Isolation - Disabled

Oracle - 0x0A2AF898cEc35197e6944D9E0F525C2626393442

eMode Category - ETH_CORRELATED

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

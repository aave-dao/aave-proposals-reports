# Proposal 86. Bounty to Hacxyk for fallback oracle misconfiguration

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=86](https://app.aave.com/governance/proposal/?proposalId=86)

### Governance forum discussion
[https://governance.aave.com/t/bgd-proposal-for-bounty-fallback-oracle-misconfiguration/8421](https://governance.aave.com/t/bgd-proposal-for-bounty-fallback-oracle-misconfiguration/8421)

<br>

## BGD analysis

### Proposal types

:money_with_wings: funds-release

### Context

This proposal releases 50'000 USDC as bug bounty for a finding of the security firm Hacxyk on the Aave v3 fallback oracle configuration.

### Proposal creation
Transaction: [https://etherscan.io/tx/0x49ab33dbc8a6804718896a2a5292aeca236816586d529f21fa98faa083c929cc](https://etherscan.io/tx/0x49ab33dbc8a6804718896a2a5292aeca236816586d529f21fa98faa083c929cc)
```
- id: 86
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xf4294973b7e6f6c411dd8a388592e7c7d32f2486]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15095971
- endBlock: 15115171
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xd7100e323d90e31a5af8b57d1ab43180ab1ffb8c7a3a53daa311bfe909fff365
```

### Aave Seatbelt report
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/p-86/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/086.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/p-86/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/086.md)

### Technical analysis

**DISCLOSURE. BGD has submitted this proposal**
From a technical perspective, we have verified that the proposal payload does the following:

1. Transfers 50'000 aUSDC to the governance short executor from the [Aave V2 Ethereum Collector](https://etherscan.io/address/0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c#code), by calling `transfer()` on the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code).

2. Withdraws 50'000 USDC from the Aave V2 Ethereum [Pool](https://etherscan.io/address/0x7d2768dE32b0b80b7a3454c06BdAc94A69DDc7A9#code), to the funds recipient account defined on the payload.


### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD wrote the payload.

:white_check_mark: With BGD writing the payload, at least another party reviewed it.

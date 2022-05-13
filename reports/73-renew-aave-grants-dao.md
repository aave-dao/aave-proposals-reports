# Proposal 73. Renew Aave Grants DAO

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=73](https://app.aave.com/governance/proposal/?proposalId=73)

### Governance forum discussion
[https://governance.aave.com/t/aave-grants-dao-update-and-renewal/7842](https://governance.aave.com/t/aave-grants-dao-update-and-renewal/7842)

<br>

## BGD analysis

### Proposal types

:money_with_wings: funds-release

:credit_card: funds-allowance

### Context
This proposal provides funding the the Aave Grants DAO for the following 6 months, in AAVE and aUSDC. 

### Technical analysis
From a technical perspective, we have verified that the payload does only 2 things:
1. Transfer of 22341.38 AAVE to a [Gnosis Safe](https://etherscan.io/address/0x89C51828427F70D77875C6747759fB17Ba10Ceb0), described as the Aave Grants DAO operational multisig.
2. Gives allowance to the aforementioned multisig for an amount of 3'000'000 aUSDC.
On both operations, the interactions happen correctly with [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code), passing the address of the [AAVE ecosystem reserve](https://etherscan.io/address/0x25F2226B597E8F9514B3F68F00f494cF4f286491#code) for the `transfer()` of AAVE and the address of the [Aave Ethereum ecosystem reserve](https://etherscan.io/address/0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c#code) for the `approve()` of aUSDC.

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:white_check_mark: Only one payload used via delegatecall

### Links
- [On-chain payload used by the proposal](https://etherscan.io/address/0x8E7DF91fEd22C192a3aA1BB6143879295EE91295#code)
# Proposal 77. Add claimRewardsToSelf() to Incentives Controller of Ethereum V2 Aave Market

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=77](https://app.aave.com/governance/proposal/?proposalId=77)

### Governance forum discussion
[https://governance.aave.com/t/proposal-adapt-contracts-slightly-to-improve-defi-composability/4125](https://governance.aave.com/t/proposal-adapt-contracts-slightly-to-improve-defi-composability/4125)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :arrow_up: contract-implementation-upgrade

<br>

### Context

Due to the architecture of Enzyme vaults, in order to claim stkAAVE rewards originated on Aave v2 Ethereum, it is not possible for their system to use the existing `claimRewards()` and `claimRewardsOnBehalf()` functions, as on those it is not possible to enforce that the claimer, address accruing the rewards and beneficiary of them are the same address: `msg.sender`.

This proposals adds a `claimRewardsToSelf()` on which all of the 3 aforementioned entities are the same, factually implementing a more restrictive "claiming" function, but necessary due to the nature of the Enzyme system (and potentially others, with similar trust assumptions).

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0x3706ac0fd5feb96f3315482fd07b7330fc654023f605358ef49ebfd40c25a722](https://etherscan.io/tx/0x3706ac0fd5feb96f3315482fd07b7330fc654023f605358ef49ebfd40c25a722)
```
- id: 77
- creator: 0x775116496f2e8fee8d6a425f1327e48aabec035b
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xb8fa635fec4e6bdb05e7937cbef01214991e9d5a]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 14836163
- endBlock: 14855363
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xbcb3635cddd0d4de418c48e98e1a8af8dd2278db1e1cc4f05de387f7bdd1d794

```

<br>

### Technical analysis
From a technical perspective, the proposal consists in an update of a proxy implementation, of the `StakedTokenIncentivesController` that manages the stkAAVE rewards' distribution on Aave v2 Ethereum.

BGD has verified that the only changes respect to the previous implementation are the ones observable [HERE](https://github.com/aave/incentives-controller/pull/4/files), said:
- Increase of the REVISION to 2, necessary to any update of a proxy's implementation.
- Remove content within `initialize()`, as there is nothing to do at initialization of this new version.
- Addition of a `claimRewardsToSelf()` function, enforcing the usage of `msg.sender` for all entities involved in the claim (via the internal `_claimRewards()`).

We have also verified that the changes on that PR are exactly the same as on the deployed smart contract to be used on [https://etherscan.io/address/0xD9ED413bCF58c266F95fE6BA63B13cf79299CE31#code](https://etherscan.io/address/0xD9ED413bCF58c266F95fE6BA63B13cf79299CE31#code).

Regarding the proposal's payload, as expected it only calls `setAddressAsProxy()` on the [Pool Addresses Provider](https://etherscan.io/address/0xB53C1a33016B2DC2fF3653530bfF1848a515c8c5#code) of Aave v2 Ethereum. Function used to update the implementation under a proxy controlled by the Pool Addresses Provider.

In addition, we are aware that the proposal has:
- A security review, with the final report [HERE](https://github.com/aave/incentives-controller/blob/1ef7705546dc7970795003e435f76b73efebbb1d/audits/Enzyme_Aave_IncentivesController_Improvement.pdf).
- A suite of unit and "fork" tests, visible on the previously mentioned Pull Request [HERE](https://github.com/aave/incentives-controller/pull/4/files).

<br>

<br>
<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed that the contract update doesn't affect proxy's storage layout.

:white_check_mark: BGD reviewed that there is no attack involving a non-initialized proxy's implementation.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:white_check_mark: Additional assurance of a security review by a third-party auditor (MixBytes).

:white_check_mark: Only one payload used via delegatecall

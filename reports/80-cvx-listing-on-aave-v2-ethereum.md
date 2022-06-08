# Proposal 80. Listing of CVX on Aave v2 Ethereum

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=80](https://app.aave.com/governance/proposal/?proposalId=80)

### Governance forum discussion
[https://governance.aave.com/t/arc-add-support-for-cvx-convex-finance-token/7319](https://governance.aave.com/t/arc-add-support-for-cvx-convex-finance-token/7319)

<br>

## BGD analysis

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

### Context

This proposal lists the [CVX][https://etherscan.io/address/0x4e3fbd56cd56c3e72c1403e103b45db9da5b9d2b] asset into Aave v2 Ethereum.

### Proposal creation
Transaction: [https://etherscan.io/tx/0x1aa05cd2665c754330d873096892ab0fef2de16135e7dacfbd3d808489e3f659](https://etherscan.io/tx/0x1aa05cd2665c754330d873096892ab0fef2de16135e7dacfbd3d808489e3f659)
```
- id: 80
- creator: 0x5b3bffc0bcf8d4caec873fdcf719f60725767c98
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xe775a3a0a1cdc50bd48d5f47c442a0a4f5f24473,0xa50ba011c48153de246e5192c8f9258a2ba79ca9]
- values: [0,0]
- signatures: [execute(address,address,address,address,address,uint256,uint256,uint256,uint256,uint8,bool,bool,bool),setAssetSources(address[],address[])]
- calldatas: [0x0000000000000000000000004e3fbd56cd56c3e72c1403e103b45db9da5b9d2b0000000000000000000000000e9134467a273de42be82d8764bf1e9cc0e0c8ba00000000000000000000000010638c31daeee246f0026f7174e1f30fb17010f5000000000000000000000000a2ec40e5e60d71144e16c92a4c78f8b38fea78770000000000000000000000001da981865ae7a0c838efbf4c7dfecb5c7268e73a000000000000000000000000000000000000000000000000000000000000119400000000000000000000000000000000000000000000000000000000000017700000000000000000000000000000000000000000000000000000000000002a6200000000000000000000000000000000000000000000000000000000000007d00000000000000000000000000000000000000000000000000000000000000012000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001,0x0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000004e3fbd56cd56c3e72c1403e103b45db9da5b9d2b0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000c9cbf687f43176b302f03f5e58470b77d07c61c6]
- withDelegatecalls: [true,false]
- startBlock: 14922542
- endBlock: 14941742
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x8346fdee34f7a14f3293ddc57b74e15d3194beee0c6db998a2dd43418cc907b2
```

### Aave Seatbelt report
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/080.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/080.md)

### Technical analysis
This proposal lists CVX, by using the generic listing payload [AssetListingProposalGenericExecutor](https://etherscan.io/address/0xe775A3A0A1cdc50bD48d5F47c442A0a4F5F24473#code) and by setting a Chainlink price feed CVX/ETH as price source on the Aave oracle.
We have verified that the listing parameters are consistent with the ones defined on the forum, being:
- **LTV**: 45%
- **Liquidation Threshold**: 60%
- **Liquidation Bonus**: 8.5%
- **Reserve Factor**: 20%
- **Enabled to borrow**.
- **Not enabled to borrow at stable mode**.
We have also verified that the proposal configures correctly the price feed CVX/ETH.

Some remarks from BGD:
- It is possible that the risk parameters are not properly adjusted for the current moment, as they were suggested on April 2th, and the market has changed importantly in the last 2 months. Given they are conservative enough, it is perfectly acceptable, but we recommend the risk arm of the community to review and potentially modified them post-listing.
- This proposal's payload is a multi-step one: first it executes the listing on the LendingPoolConfigurator, then it calls the AaveOracle to set the price source for CVX. Given the atomicity guaranteed by the AaveGovernance and its executors, this is perfectly safe. But we highly discourage to do it on this order, and setting the price feed first, as the Aave pool system was designed to always have a proper price feed before an asset gets listed/configured. Having this as common practise could lead to problems down the line.
- We also recommend to initialize the implementations of aTokens and debtTokens. There is no attack vector via non-initialization there, but it is a good security-hygiene practise.

<br>
<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed that there is no attack involving a non-initialized proxy's implementation.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:white_check_mark: Payload encoded via delegatecall + call.

:x: BGD reviewed the payload before the proposal was submitted.

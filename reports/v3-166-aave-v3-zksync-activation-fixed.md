# Proposal 166. Aave v3 zkSync Activation - re-deployment.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=166](https://vote.onaave.com/proposal/?proposalId=166)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-deployment-of-aave-on-zksync/17937](https://governance.aave.com/t/arfc-deployment-of-aave-on-zksync/17937)

<br>

### Payloads

* zkSync - [proposal payloads](https://era.zksync.network//address/0x14A2aBb02E5C5fA9890ae831A7EAdAc7846923c3#code#F1#L72)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

:handshake: permission granting or revoking

:gem: :new: asset-listing

<br>

### Context

This proposal deploys Aave V3 on zkSync to leverage the scalability and cost-efficiency of zk-Rollups, by listing the USDC, USDT, WETH, wstETH, ZK assets. The proposal redeploys proposal 153 in after the fix to the issue on the dependencies of the ZkSync Era compiler.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb3e30ec738bff9bfbbf15aea1bca0cac34bbf9e1c8bc02aca3550b931045865d](https://etherscan.io/tx/0xb3e30ec738bff9bfbbf15aea1bca0cac34bbf9e1c8bc02aca3550b931045865d)

```
- proposalId: 166
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x93d05154849d2134ec4599cfc4e9da9755b3a47d30d9db27d2f2ea2a1b3d98b6
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "324", 
      "accessLevel": "1", 
      "payloadsController": "0x2E79349c3F5e4751E87b966812C9E65E805996F1", 
      "payloadId": "4" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x93d05154849d2134ec4599cfc4e9da9755b3a47d30d9db27d2f2ea2a1b3d98b6" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/166.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/166.md)

**Payload reports**


<br>

### Technical analysis

We have verified that the payload setting up the parameters correctly to each asset. We have verfied that the payload set the gaurdian as the pool admin and that ACI_MULTISIG is set as the Emission Admin.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum, except for the supply and borrow cup which have been changed to aprroximently 10,000$ in value in order to technical providers confirm everything working correctly.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

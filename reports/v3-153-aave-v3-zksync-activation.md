# Proposal 153. Aave v3 zkSync Activation.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=153](https://vote.onaave.com/proposal/?proposalId=153)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-deployment-of-aave-on-zksync/17937](https://governance.aave.com/t/arfc-deployment-of-aave-on-zksync/17937)

<br>

### Payloads

* zkSync - [proposal payloads](https://era.zksync.network//address/0xB8c88b80f3bd77fa0Ea7DC831549e9bdcC024DF3#code#F1#L176)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

:handshake: permission granting or revoking

:gem: :new: asset-listing

<br>

### Context

This proposal deploys Aave V3 on zkSync to leverage the scalability and cost-efficiency of zk-Rollups, by listing the USDC, USDT, WETH, wstETH, ZK assets.

<br>

### Proposal creation

Transaction: [https://era.zksync.network//tx/0xdd46911b409d56cccd0461a01d8c84ac0437ce739e30ceeacb7e3dd55a088929](https://era.zksync.network//tx/0xdd46911b409d56cccd0461a01d8c84ac0437ce739e30ceeacb7e3dd55a088929)

```
- proposalId: 153
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x8688fbcdbef567e630198b664e826823dc48b4da2db2935ef827664a25dfce42
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
      "payloadId": "2" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x8688fbcdbef567e630198b664e826823dc48b4da2db2935ef827664a25dfce42" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/153.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/153.md)

**Payload reports**


<br>

### Technical analysis

We have verified that the payload setting up the parameters correctly to each asset. We have verfied that the payload set the gaurdian as the pool admin and that ACI_MULTISIG is set as the Emission Admin.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

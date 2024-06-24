# Proposal 123. Set ACI as Emission Manager on the Avalanche network.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=123](https://vote.onaave.com/proposal/?proposalId=123)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-set-aci-as-emission-manager-for-liquidity-mining-programs/17898/4](https://governance.aave.com/t/arfc-set-aci-as-emission-manager-for-liquidity-mining-programs/17898/4)

<br>

### Payloads

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x27f7Eb44eFdB4fcE580D7A81Ccb8f4528CA3102F/contract/43114/code)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal sets ACI multisig as the emission manager of wAVAX, ggAVAX and sAVAX on the Avalanche network in order to distribute rewards to users, which will incentivize more engagement with the protocol.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3e642b2db470dcccd44e98d634cae51cfaf91a6a2933d967236269a95058cec8](https://etherscan.io/tx/0x3e642b2db470dcccd44e98d634cae51cfaf91a6a2933d967236269a95058cec8)

```
- proposalId: 123
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x3549dd6b5451ee288560662dbc7b89e97d647424b6606d253445087028d15ba5
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "39" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x3549dd6b5451ee288560662dbc7b89e97d647424b6606d253445087028d15ba5" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/123.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/123.md)

**Payload reports**

* Avalanche V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/39.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/39.md)

<br>

### Technical analysis

We have verified that the ACI multisig address was set to be the emission manager of wAVAX, ggAVAX and sAVAX on the Avalanche network.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

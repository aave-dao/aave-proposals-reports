# Proposal 171. Set ACI as Emission Manager for wstETH & tBTC on Ethereum Mainet and Lido Instances.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=171](https://vote.onaave.com/proposal/?proposalId=171)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-set-aci-as-emission-manager-for-liquidity-mining-programs/17898/15](https://governance.aave.com/t/arfc-set-aci-as-emission-manager-for-liquidity-mining-programs/17898/15)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xCC01d14Caa28F7FB6A638587E829E7E4bF22616f#code#F1#L17)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal sets ACI multisig as the emission manager of wstETH and tBTC on the Ethereum Maintet and Lido instances in order to distribute rewards to users, which will incentivize more engagement with the protocol.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x121628b466a0b184587977432ac9021e4aef8036d22da892ced40372cb8fe0e6](https://etherscan.io/tx/0x121628b466a0b184587977432ac9021e4aef8036d22da892ced40372cb8fe0e6)

```
- proposalId: 171
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x243c4732500e528f9bd74a2f0a761c4b5ace944f6036e352634c7e2ba3e0fa25
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
      "payloadId": "179" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x243c4732500e528f9bd74a2f0a761c4b5ace944f6036e352634c7e2ba3e0fa25" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/171.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/171.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/179.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/179.md)

<br>

### Technical analysis

We have verified that the ACI multisig address was set to be the emission manager of wstETH and tBTC on the Ethereum network.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

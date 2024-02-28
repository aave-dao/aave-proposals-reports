# Proposal 37. Aave V1 Deprecation Phase 2.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=37](https://vote.onaave.com/proposal/?proposalId=37)

<br>

### Governance forum discussion

[https://governance.aave.com/t/temp-check-bgd-further-aave-v1-deprecation-strategy/15893/5](https://governance.aave.com/t/temp-check-bgd-further-aave-v1-deprecation-strategy/15893/5)

<br>

### Payloads

[proposal payloads](https://etherscan.io/address/0xc3A6c8719Bdb1A4f78Fa0a4DD46301c73EE23a90#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: contract upgrade

<br>

### Context

This proposal upgrades the liquidation manager to allow liquidation of healthy positions with a fixed 3% bonus, as further step of Aave v1 off-boarding, to reduce operational overhead on deprecated Aave instances.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1891c87d6ebbef539edd1ed56299b4012a02a5c84e59f71f9c7fc815ea0b1de0](https://etherscan.io/tx/0x1891c87d6ebbef539edd1ed56299b4012a02a5c84e59f71f9c7fc815ea0b1de0)

```
- proposalId: 37
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xa451c9a2426267673fd125702c99581683426ca5ff1a003b07a3cd129ed30470
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
      "payloadId": "67" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xa451c9a2426267673fd125702c99581683426ca5ff1a003b07a3cd129ed30470" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/37.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/37.md)

**Payload reports**

* Ethereum V1 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/67.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/67.md)

<br>

### Technical analysis

We have verified that the payload upgrades the LIQUIDATION_MANAGER contract to the one specified in the IPFS with the new implementation having 3% bonus on liquidation and revision 2.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

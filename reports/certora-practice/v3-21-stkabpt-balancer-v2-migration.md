# Proposal 21. stkABPT Balancer V2 migration.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=21](https://vote.onaave.com/proposal/?proposalId=21)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-abpt-balancer-v2-migration-plan/8381/7#abpt-balancer-v1-v2-migration-update-1](https://governance.aave.com/t/bgd-abpt-balancer-v2-migration-plan/8381/7#abpt-balancer-v1-v2-migration-update-1)

<br>

### Payloads

[proposal payloads](https://etherscan.io/address/0xFfC6788753444Ad4023C9fc0D5820E3a1887519B#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: contract upgrade

<br>

### Context

This proposal will deprecate stkABPT balancer-v1 safety module for a new version AAVE_wstETH_BPT_V2 Balancer v2 safety module in order to yield optimized AAVE/wstETH pool.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3d9300ddd40c3115a74953a858ae0d7890aac81cddbabed6fc57ffea55134da3](https://etherscan.io/tx/0x3d9300ddd40c3115a74953a858ae0d7890aac81cddbabed6fc57ffea55134da3)

```
- proposalId: 21
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x15ad1b6f904ccd31e1419f0440efa53d9f4f723074f1566109fbff1255945a9d
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
      "payloadId": "56"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x15ad1b6f904ccd31e1419f0440efa53d9f4f723074f1566109fbff1255945a9d"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/21.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/56.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/56.md)

<br>

### Technical analysis

We have verified that the payloads executing the following steps:

- disables the cooldown by upgrading the implementation of stkABPT-v1.

- stops emission on module v1.

- starts emission on module v2.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

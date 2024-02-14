# Proposal 22. Migration of remaining Gov v2 permissions & DAO's Paraswap positive slippage.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=22](https://vote.onaave.com/proposal/?proposalId=22)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/17](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/17)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xd15280055CfE8A8AD69EBC5108582fE5CF9e72ae#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

:handshake: permission granting or revoking

<br>

### Context

This proposal the following actions in order to migrate Aave Arc pool permissions & Paraswap positive slippage funds allocated to the old governance v2 Short Executor:

- claims some funds (~100k) which are pending to claim from the previous system which still need migration.

- migrates some permissions of Aave Arc pool to the new governance system.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x38de005179e11db15d5822d0201f92ebd1f18292a9e27179df157d84d5c3feee](https://etherscan.io/tx/0x38de005179e11db15d5822d0201f92ebd1f18292a9e27179df157d84d5c3feee)

```
- proposalId: 22
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xfbdf952d057c250d16c9f04e17f628b605bf72e348704da5809fbaf9bbafe684
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
      "payloadId": "57"
    },
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
      "payloadId": "58"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xfbdf952d057c250d16c9f04e17f628b605bf72e348704da5809fbaf9bbafe684"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/22.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/22.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/57.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/57.md)

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/58.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/58.md)

<br>

### Technical analysis

We have verified that the payloads executing the following actions:

- claim pending rewards to the collector of all tokens available.

- migrates some permissions of the deprecated Aave Arc pool to the new governance system-V3.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

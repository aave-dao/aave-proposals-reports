# Proposal 15. Aave V1 Deprecation

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=15](https://vote.onaave.com/proposal/?proposalId=15)

<br>

### Governance forum discussion

[https://governance.aave.com/t/temp-check-bgd-further-aave-v1-deprecation-strategy/15893](https://governance.aave.com/t/temp-check-bgd-further-aave-v1-deprecation-strategy/15893)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xa4979A7B7c00080142f2D9bc3247735b15c64005#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking
:handshake: contract upgrade

<br>

### Context

This proposal continues the aave v1 off-boarding by upgrading the pool logic

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5d5de851d34a5826abd24e9c78947a46672207635e9a3f4c23a3fe3ccb0d1e06](https://etherscan.io/tx/0x5d5de851d34a5826abd24e9c78947a46672207635e9a3f4c23a3fe3ccb0d1e06)

```
- proposalId: 15
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x8436f643b0e21810e207abe3d975fa647a4e0748a49ee9761a79366886b71789
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
      "payloadId": "54"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x8436f643b0e21810e207abe3d975fa647a4e0748a49ee9761a79366886b71789"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/15.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/15.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/54.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/54.md)

<br>

### Technical analysis

We have verified that the payloads executing the following steps:

- setting up a new liquidation manager contract.

- setting up a new pool contract.

- setting up new reserve interest rate strategy on all the tokens with 0% base and 1%/2% slopes.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

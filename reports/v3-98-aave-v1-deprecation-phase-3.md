# Proposal 98. Aave V1 Deprecation Phase 3.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=98](https://vote.onaave.com/proposal/?proposalId=98)

<br>

### Governance forum discussion

[https://governance.aave.com/t/temp-check-bgd-further-aave-v1-deprecation-strategy/15893/7](https://governance.aave.com/t/temp-check-bgd-further-aave-v1-deprecation-strategy/15893/7)

<br>

### Payloads

* Ethereum V1 - [proposal payloads](https://etherscan.io/address/0x9cCC75B3770C892081F3dF960F1490e8B5A592fd#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade

<br>

### Context

This proposal is the third and final step of Aave V1 deprecation in order to reduce operational overhead on deprecated Aave instances.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x77d4f24a12c25cf8a1def7307f5819c51e021216ecd855e8c6b540065b3a515b](https://etherscan.io/tx/0x77d4f24a12c25cf8a1def7307f5819c51e021216ecd855e8c6b540065b3a515b)

```
- proposalId: 98
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x01f7e5f64c1d7265381681d7090612d3da8fda9ef37b0db36c9e15e119d3a0c7
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
      "payloadId": "120" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x01f7e5f64c1d7265381681d7090612d3da8fda9ef37b0db36c9e15e119d3a0c7" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/98.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/98.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/120.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/120.md)

<br>

### Technical analysis

We have verified that the payload Updates the pool implementation, the pool-core implementation and the pool-liquidation-manager implementation with the following:

- Core:

    the new implementation will be up to date with the pool implementation in order to update the index upon IR updates.

- Poll:

    the new implementation disables all actions, but liquidation, repay and withdraw.

- Liquidation-Manager:

    the new implementation brings static liquidation penalty from 3% to 5%, while reducing the gas overhead.

We have also verified that all the assets of V1 will be updated to have zero interest strategy and that the stablecoin oracles are replaced with the capped oracles which are used on ethereum v2.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

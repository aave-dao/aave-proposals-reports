# Proposal 336. CEX Earn Funding Proposal

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=336)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-gho-cex-earn-incentive-program/22284)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x5355336aaF7DbB6E67C2237a9D0d0d7A3f96d0b3)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking



### Context
To maximize the impact of GHO’s upcoming listings on Bybit, Bitget, and other centralized exchanges (CEXs), this publication proposes engaging a market maker to provide spot liquidity and allocating funds to a CEX Earn program to drive broader adoption of GHO.

### Proposal Creation
Transaction: [0x58ee09f482e83b51f68c20cb6594f86e74ad143485bf6f0d851434ee24165e27](https://etherscan.io/tx/0x58ee09f482e83b51f68c20cb6594f86e74ad143485bf6f0d851434ee24165e27)
- `proposalId`: 336
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x8b5aea7c778b9b4a2367ae2ffd6ad34f21aeb899933b28353ef5f0cca6c5f4eb

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 312,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x8b5aea7c778b9b4a2367ae2ffd6ad34f21aeb899933b28353ef5f0cca6c5f4eb",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/336.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/312.md)


### Technical Analysis
We have validated the addresses and the amounts.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 375. Add EURC to Avalanche V3 Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=375)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-add-eurc-to-avalanche-v3-instance/21734)

### Payloads

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xe8b8bfCB8377660936C305533a28dB7B341cb53E)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
The current ARFC proposes to add `EURC` on Avalanche V3 Instance. `EURC` is Circle’s EUR-backed stablecoin, enhancing liquidity and expanding the platform’s appeal to European users.

### Proposal Creation
Transaction: [0x668b3a501f3ff435bd8ff187cab6046cd905c712e497446083ba4fe99f1ec017](https://etherscan.io/tx/0x668b3a501f3ff435bd8ff187cab6046cd905c712e497446083ba4fe99f1ec017)
- `proposalId`: 375
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x092b9dcb1a0b1f557c7bd7139b1ada7ccdce95a545bdb8327e8a3a0d11c75042

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 95,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x092b9dcb1a0b1f557c7bd7139b1ada7ccdce95a545bdb8327e8a3a0d11c75042",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/375.md)

**Payload Reports**

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/95.md)


### Technical Analysis
We have validated and compared the risk parameter with respect to decimal precision. We have confirmed the validity of the `EURC` address token and price feed. The seed supply was correctly implemented as well.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
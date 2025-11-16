# Proposal 407. Orbit Program Renewal - Q3 and Q4 2025

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=407)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-orbit-program-renewal-q3-and-q4-2025/23289)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x24EFBAe8Cc8f22252BA83Cac08c3341C1198e449)



## Certora Analysis

### Proposal Types


* :bank: Payment stream

### Context
Proposing the renewal of the Orbit program for recognized delegates, compensating them with GHO, associated with their governance activity during Q3 and Q4 2025 ( From 2025-07-01, last date, until 2025-12-31). The reason is because extending period coverage will bring more reliance and predictability for delegates platform.

### Proposal Creation
Transaction: [0xe05bf2fc2318ff2dded44507421b8676459f0cb5a4fd205bd60247aaffc726a0](https://etherscan.io/tx/0xe05bf2fc2318ff2dded44507421b8676459f0cb5a4fd205bd60247aaffc726a0)
- `proposalId`: 407
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x0ad339ba1cb2206e93f936589e8685fdc16d6b5beafe1f6f135768d54f2bac38

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 369,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x0ad339ba1cb2206e93f936589e8685fdc16d6b5beafe1f6f135768d54f2bac38",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/407.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/369.md)


### Technical Analysis
We have verified that the addresses match between the IPFS, payload and the forum.
We have validate all relevant addresses in the payload, the `STREAM_AMOUNT` and the unix timestamp. We have validate the payload with the seatbelt. 

The proposal is consistent with the description on both Snapshot and the governance forum.
### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
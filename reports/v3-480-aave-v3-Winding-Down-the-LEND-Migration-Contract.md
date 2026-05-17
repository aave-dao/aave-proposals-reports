# Proposal 480. Winding Down the LEND Migration Contract

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=480)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-winding-down-lend-migration-contract/23126)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4C555e9357f9cbd7235b9F3eb274eC90BF71B012)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades
* :moneybag: :receipt: Asset transfers

### Context
Terminate operations of the LEND → AAVE Migration Contract, reallocating all unspent budgets, assets, and remaining tokens or emissions into the Ecosystem Reserve, while minimizing disruption to users and integrations.

### Proposal Creation
Transaction: [0x4004d59689c69d3987c04b618b47917013766194c5212e7a0627e78b774aba3c](https://etherscan.io/tx/0x4004d59689c69d3987c04b618b47917013766194c5212e7a0627e78b774aba3c)
- `proposalId`: 480
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x1aacd2eb52a5029008ce6f8b3ea5c1da0106b254fbfb3280c67710d03e1a69e6

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 433,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x1aacd2eb52a5029008ce6f8b3ea5c1da0106b254fbfb3280c67710d03e1a69e6",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/480.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/433.md)


### Technical Analysis

We have verified that the LEND→AAVE migration proxy (`0x317625234562B1526Ea2FaC4030Ea499C5291de4`) has its implementation upgraded from `0x7b62461a3570c6AC8a9f8330421576e417B71EE7` to the new `LendToAaveMigrator` at `0x2Da544ae1EA4E19b680E7A39520c64E5D35c0345`, with the contract revision bumped from 2 to 3, consistent with the wind-down described in the AIP.

We have verified that 302,384.33 AAVE (`302384334789603807474781` wei, 18-decimal precision) is withdrawn from the migration proxy and transferred to the Aave Ecosystem Reserve (`0x25F2226B597E8F9514B3F68F00f494cF4f286491`), matching the AIP's commitment to reallocate the remaining unspent budget into the Ecosystem Reserve.

We have verified that no other balances, allowances or role assignments are mutated by the payload.

We have verified the payload's logic and validated its execution via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
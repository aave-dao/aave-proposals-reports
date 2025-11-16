# Proposal 388. Full Deprecation of DPI Across Aave Deployments

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=388)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-full-deprecation-of-dpi-across-aave-deployments/23212)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x964CF6d8d89712D2E5516ef792eA87Be9DAB16e9)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x8a697862DaF227d1FB8492D609FFe99aB6B795ac)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xb568F31C2114C34D461AC798C78F24DEa83C1C89)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal outlines the final deprecation path for DPI (DeFi Pulse Index) across all Aave deployments where it remains listed: Ethereum v2, Polygon v2, and Polygon v3. DPI has been frozen across all instances for an extended period and now represents negligible exposure within the protocol.

### Proposal Creation
Transaction: [0x86f73be6007454b4339164184125b686bdab684a145e726338d4acbd485dc44b](https://etherscan.io/tx/0x86f73be6007454b4339164184125b686bdab684a145e726338d4acbd485dc44b)
- `proposalId`: 388
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x8ba8d0d6d7f33a1f6bb82536e7d00a6ee30d8b60f5f0e04457c507b8056e6249

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 357,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 131,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 132,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x8ba8d0d6d7f33a1f6bb82536e7d00a6ee30d8b60f5f0e04457c507b8056e6249",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/388.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/357.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/131.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/132.md)


### Technical Analysis
We have verified this proposal adjust all the`DPI` instances across Aave ecosystem. We have compared the risk parameters change to the forum and the IPFS. We have checked the Fixed price feed for correctness.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 292. Caps Risk Oracle Activation on Base, Avalanche

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=292)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/78)

### Payloads

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xa7579a0fFf29304c9666337aEd374db0f2cD8217)

* Base - [proposal payloads](https://basescan.org/address/0x3ed1F3203307DC13a4770D533D59D45827B14f38)



## Certora Analysis

### Proposal Types
* :handshake: Permission granting and revoking

* :gem: :new: Listing new assets


### Context
Following the successful operation of the cap risk stewards (AGRS) on Aave v3 Arbitrum since end of February, this proposal enables exactly the same constraint system on Base and Avalanche.

### Proposal Creation
Transaction: [0xfc3fede2e1016449d581dd5c9d7894bfd1f8d1785f8136788d8d288dc7e105f0](https://etherscan.io/tx/0xfc3fede2e1016449d581dd5c9d7894bfd1f8d1785f8136788d8d288dc7e105f0)
- `proposalId`: 292
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xc4e57d0da88a6f7eb1a42d455d65adb6785158fd3152466c9e65203c5ce9c30d

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 77,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 67,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xc4e57d0da88a6f7eb1a42d455d65adb6785158fd3152466c9e65203c5ce9c30d",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/292.md)

**Payload Reports**

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/77.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/67.md)


### Technical Analysis
We have verified that the stated addresses are the upgraded contracts. We have verified the transfer of 30/50 LINK and confirmed that the registering mechanism works as intended.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
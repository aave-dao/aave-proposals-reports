# Proposal 261. Aave V2 Deprecation Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=261)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-v2-deprecation-update-disable-new-borrows-ir-curve-and-reserve-factor-adjustments/20918)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xa4D19F740935a4321c0B3688C5b1FCE1C400c8be)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x6059dAEcC34Bb90afC5841060A1949997F091c7c)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x46E8a97Cf7C553f6EB2006449346a93741e6e359)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
 Further risk parameters changes to deprecate Aave V2 protocol and encourage user migration to Aave V3


### Proposal Creation
Transaction: [0x2b371970bcfee985a6c7b98a16c43dbfbb73e0d302801e9fa8c4963dc085a811](https://etherscan.io/tx/0x2b371970bcfee985a6c7b98a16c43dbfbb73e0d302801e9fa8c4963dc085a811)
- `proposalId`: 261
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xb2c42584f134f14fb3ded36bb366465223a752d95bdb2e7aad1d9e2da76464d2

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 253,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 103,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 69,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xb2c42584f134f14fb3ded36bb366465223a752d95bdb2e7aad1d9e2da76464d2",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/261.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/253.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/103.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/69.md)


### Technical Analysis
We have verified that all the assets have been configured as specified.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
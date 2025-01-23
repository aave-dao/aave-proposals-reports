# Proposal 236. GHO Risk Stewards Update and GHO CCIP Integration Upgrade

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=236)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/59)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xD70F822Be4a18327cc0d9a2179C3da52D653f3A3)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xd1FB5b2695BEee2bBCf8ccBd3E3Ed68E0Da36bF6)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades

### Context
Update the GHO Risk Steward contracts to enhance the Risk Council’s user experience and align the design of the Risk Stewards implementations throughout the Aave Protocol.
Update the GHO CCIP Token Pools on Arbitrum and Ethereum to integrate them with latest version of CCIP (1.5.1) to leverage the full functionality of CCIP and prepare for future expansions to other chains.

### Proposal Creation
Transaction: [0x3a2dcaad061ebbc0d9e298b1323fdf6ba440259e6628e8a755ba63ab0ce68bce](https://etherscan.io/tx/0x3a2dcaad061ebbc0d9e298b1323fdf6ba440259e6628e8a755ba63ab0ce68bce)
- `proposalId`: 236
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x40c9fcf57108ed65bfc541dd4c7de318f5805f2348fa28e1a99d8a267ddbf1df

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 233,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 68,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x40c9fcf57108ed65bfc541dd4c7de318f5805f2348fa28e1a99d8a267ddbf1df",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/236.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/233.md)

* Arbitrum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/68.md)


### Technical Analysis
This proposal was audited as part of the audit of the GHO CCIP 1.5.1 upgrade the full report can be found on the full audit report for GHO CCIP 1.5.1 upgrade

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
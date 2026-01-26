# Proposal 439. Extend stkAAVE Emissions

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=439)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-amend-safety-module-emissions/16640/49)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3BC9ce8e40207a8a650BED6D756D5986725A637E)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates


### Context

Top-up the AAVE allowance for the Safety Module stkAAVE to extend rewards distribution by 90 days while keeping the current emission rate unchanged.

### Proposal Creation
Transaction: [0xc49dfb59d9ad0b4743913d822b283c75e35d47694ebc1e12ce64151fa69ef266](https://etherscan.io/tx/0xc49dfb59d9ad0b4743913d822b283c75e35d47694ebc1e12ce64151fa69ef266)
- `proposalId`: 439
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xfe12fbb0cc5b9383d0d788c9079494c1ec8d2525e05f3ff3451ea008838668b1

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 396,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xfe12fbb0cc5b9383d0d788c9079494c1ec8d2525e05f3ff3451ea008838668b1",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/439.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/396.md)


### Technical Analysis

We have confirmed that the proposal does not alter the emission rate.  
We have verified the math: `newAllowance = currentAllowance + (rate * 90 days)`.  
This accurately extends the program's runway by the intended duration.   
We have confirmed on-chain that the Ecosystem Reserve holds a sufficient AAVE balance to support the increased allowance.  
We have confirmed the approval logic and validated it through Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
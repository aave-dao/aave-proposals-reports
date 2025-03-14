# Proposal 267. GSMs Migration to stataGSM4626

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=267)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-deploy-statausdc-and-statausdt-gsms-on-ethereum/20682)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x545EF6C984E007b49524a61B8B684E2980676528)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades


### Context
Deploy two stataToken GSMs using the [ERC4626 implementation](https://governance.aave.com/t/gho-stability-module-update/14442/10) developed by Aave Labs to replace the existing USDC and USDT GSMs.

### Proposal Creation
Transaction: [0x8aef6973496ffda646fe76d0b16b6550648c2537695d50f42a5833bc64ed7072](https://etherscan.io/tx/0x8aef6973496ffda646fe76d0b16b6550648c2537695d50f42a5833bc64ed7072)
- `proposalId`: 267
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xa7a224eb00be690b558352b6afcf332e5e26693a337993e4624c78ee30fb9aeb

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 257,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xa7a224eb00be690b558352b6afcf332e5e26693a337993e4624c78ee30fb9aeb",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/267.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/257.md)


### Technical Analysis

#### Findings
During review we have found out the payload set the GSMs as GHO facilitators with the wrong bucket capacities (8M instead of 16M for USDC and 16M instead of 24M) . The fix will use the Bucket Steward that can double the amount of the bucket in each transaction.

Other than that no problem have been found. The set uo=p of the GSM was done correctly and securely.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
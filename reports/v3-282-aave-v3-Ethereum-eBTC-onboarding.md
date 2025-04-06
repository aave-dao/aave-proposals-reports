# Proposal 282. Onboard eBTC and Add eBTC/WBTC E-Mode

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=282)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-enable-ebtc-wbtc-liquid-e-mode-on-aave-v3-core-instance/20141)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x07aE852F84aD15c1A42932278D41a8b7183aeD0D)

## Certora Analysis

### Proposal Types
* :gem: :new: Listing new assets

### Context
This proposal onboard eBTC for the Core Instance, and add a WBTC liquid E-Mode. 

### Proposal Creation
Transaction: [0xfabce568d379da27f21db27f33e89ef23c4fe85ea0698ac5eb55bac6799fd033](https://etherscan.io/tx/0xfabce568d379da27f21db27f33e89ef23c4fe85ea0698ac5eb55bac6799fd033)
- `proposalId`: 282
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xf4d0bfca8139dbf720019bd9517e23396e9217e223f9b7ecceca2903667ad088

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 262,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xf4d0bfca8139dbf720019bd9517e23396e9217e223f9b7ecceca2903667ad088",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/282.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/262.md)


### Technical Analysis
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
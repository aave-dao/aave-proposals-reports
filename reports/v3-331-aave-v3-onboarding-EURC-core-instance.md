# Proposal 331. Add EURC to Aave V3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=331)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-add-eurc-to-aave-v3-core-instance/21837)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xe690bcd2a4048b3CF9BE0FcaACc6EACE6bEfB41B)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
The current AIP proposes to add EURC on Aave V3 Core Instance.

EURC is Circle’s EUR-backed stablecoin, enhancing liquidity and expanding the platform’s appeal to Euro denominated users.

### Proposal Creation
Transaction: [0x7fe131b7409f14e748885e2bda08f2fd23f35ebbf7417bfd105568dc0c7ce329](https://etherscan.io/tx/0x7fe131b7409f14e748885e2bda08f2fd23f35ebbf7417bfd105568dc0c7ce329)
- `proposalId`: 331
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xf93eb58ea5cf5aaf82c5e3c799ac717bed7c1879c6a4ae1525087df7a873e5b6

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 310,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xf93eb58ea5cf5aaf82c5e3c799ac717bed7c1879c6a4ae1525087df7a873e5b6",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/331.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/310.md)


### Technical Analysis
We have verified the risk parameters are equal to the specification. The seed amount is transferred correctly.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
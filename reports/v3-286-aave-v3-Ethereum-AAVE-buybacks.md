# Proposal 286. AAVE Buybacks allocation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=286)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aavenomics-implementation-part-one/21248)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x01A2073b8C26814E170C81ae97c41B5723Cb3602)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking


### Context
This proposal approves a specific allowance of aEthUSDT from the Aave Collector contract to the Aave Finance Committee (AFC), enabling the committee to initiate AAVE buybacks as part of the Aavenomics implementation

### Proposal Creation
Transaction: [0x29e5f525f3453b32d94f5596518fc1c7832b78894fa688d75de9a273e41b9aa1](https://etherscan.io/tx/0x29e5f525f3453b32d94f5596518fc1c7832b78894fa688d75de9a273e41b9aa1)
- `proposalId`: 286
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x7b3631f33440766118f881b34797f01d87602887d1204ec83883778a947f7154

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 267,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x7b3631f33440766118f881b34797f01d87602887d1204ec83883778a947f7154",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/286.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/267.md)


### Technical Analysis
We have confirmed the amount and address are as specified in the ipfs and forum.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
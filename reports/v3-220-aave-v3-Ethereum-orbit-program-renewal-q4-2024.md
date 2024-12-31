# Proposal 220. Orbit Program Renewal - Q4 2024

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=220)

### Governance Forum Discussions
[Link to forum discussions](https://governance.aave.com/t/arfc-orbit-program-renewal-q4-2024/20084)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x06ec9f978FA92d45544ae1A63ba2E86d2cC37C05)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers

* :bank: payment stream

### Context
Proposing the renewal of the Orbit program for recognized delegates, compensating them with GHO, associated with their governance activity during Q4 2024 ( From 2024-08-31 to 2024-12-14). 

### Proposal Creation
Transaction: [0x24525b9d552e1e6e76096b1f1f9368f864c2726c26d497434768ec0732b4c589](https://etherscan.io/tx/0x24525b9d552e1e6e76096b1f1f9368f864c2726c26d497434768ec0732b4c589)
- `proposalId`: 220
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xa65981356b7309a6b13687ecc05aa4a3d973771c3c61e6ebf908759f2403bd23

**`createProposal()` Parameters**
```
{
    "payloads": [
        {
            "chain": "1",
            "accessLevel": 1,
            "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            "payloadId": 223
        }
    ],
    "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    "ipfsHash": "0xa65981356b7309a6b13687ecc05aa4a3d973771c3c61e6ebf908759f2403bd23"
}
```

### Aave Seatbelt Report
**Proposal Report**
[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/220.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/223.md)


### Technical Analysis
The technical review confirms that all aspects of the proposal have been implemented as intended. The amounts transferred align accurately with the proposed budget, and the GHO stream has been successfully created on the Prime Instance. The stream duration is configured correctly to match the specified 80-day period, ensuring steady compensation throughout the quarter. Additionally, the addresses of the recognized service providers have been verified and match those listed in the proposal. Overall, the execution adheres to the proposal’s specifications without discrepancies.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
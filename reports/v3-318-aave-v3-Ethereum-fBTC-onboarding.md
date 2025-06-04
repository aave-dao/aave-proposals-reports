# Proposal 318. Add FBTC to Aave v3 Main Market on Ethereum

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=318)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-add-fbtc-to-aave-v3-main-market-on-ethereum/19937)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x17ce289A8B29c0db24a024fC9F399026EcA45992)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
The proposal aims to onboard Ignition’s FBTC, to the Aave v3 protocol Main Market on Ethereum.


### Proposal Creation
Transaction: [0xec2e8ac65bdcb3b58466e4706542f28e3f93cdb3ba645e0c14aa880242469b12](https://etherscan.io/tx/0xec2e8ac65bdcb3b58466e4706542f28e3f93cdb3ba645e0c14aa880242469b12)
- `proposalId`: 318
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xda3df9ee07c5133298cfe63fb0745b5f227ea5a27c009d89242246379c951402

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 294,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xda3df9ee07c5133298cfe63fb0745b5f227ea5a27c009d89242246379c951402",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/318.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/294.md)


### Technical Analysis

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
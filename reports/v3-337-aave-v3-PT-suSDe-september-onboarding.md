# Proposal 337. Onboard sUSDe September expiry PT tokens on Aave V3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=337)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-susde-september-expiry-pt-tokens-on-aave-v3-core-instance/22313)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x86b4bBCf2071494B3dB77B08fe4fb8c7BF145052)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This AIP proposes to onboard sUSDe September expiry PT tokens on Aave V3 Core Instance.

### Proposal Creation
Transaction: [0xbf99d7be45ba556eac034f281cf3ac28b03cbb6812100663323f7e72828626a8](https://etherscan.io/tx/0xbf99d7be45ba556eac034f281cf3ac28b03cbb6812100663323f7e72828626a8)
- `proposalId`: 337
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xdd71ef33885a0eedf87855c16fdf3f6ae2ea1268dcc35d76888cfb6fa1b41ce6

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 315,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xdd71ef33885a0eedf87855c16fdf3f6ae2ea1268dcc35d76888cfb6fa1b41ce6",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/337.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/315.md)


### Technical Analysis
We have verified that the risk parameters match those specified in the IPFS. The price oracle configuration has been validated for correctness, and the E-mode categories have been confirmed as correctly created.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
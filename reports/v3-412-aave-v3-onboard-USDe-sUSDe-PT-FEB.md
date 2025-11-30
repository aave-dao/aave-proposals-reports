# Proposal 412. Ethena PT FEB Listing

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=412)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-usde-susde-february-expiry-pt-tokens-on-aave-v3-core-instance/23358)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xC0154D0017074D93CB17D8b122d2E682e2354B01)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets

### Context
This AIP proposes to onboard USDe and sUSDe February expiry PT tokens on Aave V3 Core Instance.

This proposal is Direct to AIP.

### Proposal Creation
Transaction: [0xbb9993d432442387414a215d2b601b22164b2de87815eb0960a6fecf7e78c69a](https://etherscan.io/tx/0xbb9993d432442387414a215d2b601b22164b2de87815eb0960a6fecf7e78c69a)
- `proposalId`: 412
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x6bd0de6474e78b0e46734f35fa07972fad2a9d3991122427130cb0cd9ea9c2b3

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 372,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x6bd0de6474e78b0e46734f35fa07972fad2a9d3991122427130cb0cd9ea9c2b3",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/412.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/372.md)


### Technical Analysis
We have verified the addresses of the new assets, their expiry dates, and their oracles.
We validated the payload logic and its execution via Seatbelt. We also verified the seed amounts with respect to decimals.
We checked for consistency between the forum, IPFS, and the payload. We found a few typos and contacted ACI.
Overall, the proposal is consistent with the descriptions on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 365. Onboard sUSDe November expiry PT tokens on Aave V3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=365)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-susde-november-expiry-pt-tokens-on-aave-v3-core-instance/22894)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x1bfeE8961311825d962Bbe8D8D76b23F2AA288D7)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This AIP proposes to onboard sUSDe November expiry PT tokens on Aave V3 Core Instance.

### Proposal Creation
Transaction: [0xacc9f10933a2f68bcecd92e5ef21f7e2fec022bfd3461a097c2d0d4c2a378a93](https://etherscan.io/tx/0xacc9f10933a2f68bcecd92e5ef21f7e2fec022bfd3461a097c2d0d4c2a378a93)
- `proposalId`: 365
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xab3ff6fed787c72953538ff886e858da200d500887c9a7868d320a3dc8eba4f1

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 334,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xab3ff6fed787c72953538ff886e858da200d500887c9a7868d320a3dc8eba4f1",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/365.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/334.md)


### Technical Analysis
We have verified the risk parameters match the forum and the IPFS, we have validated the addresses of the token and the price feeds for correctness (by looking for them in there respective source of truth), we have confirmed the modes were created to new IDs.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
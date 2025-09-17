# Proposal 367. Onboard USDe November expiry PT tokens on Aave V3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=367)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-usde-november-expiry-pt-tokens-on-aave-v3-core-instance/23013)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4D91EC50007F79FfB71b3C8CFB733D46c4C1fe9d)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This AIP proposes to onboard USDe November expiry PT tokens on Aave V3 Core Instance.

### Proposal Creation
Transaction: [0xf3ecf481143698d848f8b9aaf4d966edac025add89c0d9c482e599bccfd2a500](https://etherscan.io/tx/0xf3ecf481143698d848f8b9aaf4d966edac025add89c0d9c482e599bccfd2a500)
- `proposalId`: 367
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x1cbc2ec9f75d0cb82a860e44d27ae8e7d303bb044bb4d9d27ece5fc3e09d7350

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 337,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x1cbc2ec9f75d0cb82a860e44d27ae8e7d303bb044bb4d9d27ece5fc3e09d7350",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/367.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/337.md)


### Technical Analysis
We verified each address, role, and price feed against on-chain sources of truth and the Aave address book. We checked token metadata and units, including decimals, scaling, interest rate curve, LTV, LT, liquidation bonus, caps, borrow flags, and oracle discount settings. We compared the spec to the payload for e-mode composition, injector whitelists, and the small 100 PT seed deposit, confirming alignment.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 347. wS and BTC.b Interest Rate Curve Optimization

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=347)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-ws-and-btc-b-interest-rate-curve-optimization/21962)

### Payloads

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xAabf595d5560e58356315f9807FD1D9f7DaE347d)

* Sonic - [proposal payloads](https://sonicscan.org/address/0x9Ce6b5B055113AB732B88cE3e4Dce3186951AAeD#code)


## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
{**TODO: Write context.**}

### Proposal Creation
Transaction: [0x4e43255e8f4751ae8c6d336cf9efd5ff0e9bf26d701d9adb5ea1ffcd866f51b1](https://etherscan.io/tx/0x4e43255e8f4751ae8c6d336cf9efd5ff0e9bf26d701d9adb5ea1ffcd866f51b1)
- `proposalId`: 347
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x4a6f5b9db43af90aa99020adf1195e04a8e9a96f171847f85ec7848f1c2c3ac1

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 90,
        },
        {
            chain: "146",
            payloads_controller: "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695",
            payload_id: 8,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x4a6f5b9db43af90aa99020adf1195e04a8e9a96f171847f85ec7848f1c2c3ac1",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/347.md)

**Payload Reports**

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/90.md)

* Sonic - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/146/0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695/8.md)

### Technical Analysis
We have verified the risk parameters have configured correctly with respect to decimal precision.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
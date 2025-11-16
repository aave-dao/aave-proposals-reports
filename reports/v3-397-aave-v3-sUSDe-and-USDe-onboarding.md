# Proposal 397. Onboard sUSDe and USDe to Aave V3 Avalanche Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=397)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-susde-and-usde-to-aave-v3-avalanche-instance/23081)

### Payloads

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x951188578692Fa789F98c0e07374C6598DF4aB57)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This proposal seeks to onboard sUSDe and USDe to the Aave v3 protocol on Avalanche.The onboarding of sUSDe and USDe to the Aave Avalanche Instance will provide users with high quality yield bearing stablecoin collateral to help expand stablecoin usage on this instance.

As the Avalanche instance shows promise and potential for significant growth we believe the time is right for expanding collateral options on this network with a focus on those assets which have proven to be in demand on other Aave instances.

Ava Labs has committed 1000 AVAX per week in incentives to bootstrapping usage of these assets on the Avalanche Aave instance.

### Proposal Creation
Transaction: [0x393ad8280f2b93789a7456d99c0084846a3a7c4dddc829b9ca7a5c7702e86220](https://etherscan.io/tx/0x393ad8280f2b93789a7456d99c0084846a3a7c4dddc829b9ca7a5c7702e86220)
- `proposalId`: 397
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x1f54d6a74f565aadaa76ec5ca40c839f6fdb17cf48a365c4fade77fc6bd7dc28

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 100,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x1f54d6a74f565aadaa76ec5ca40c839f6fdb17cf48a365c4fade77fc6bd7dc28",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/100.md)

**Payload Reports**

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/100.md)


### Technical Analysis

We have validated and compared the risk parameter with respect to decimal precision. We have confirmed the validity of the `sUSDe` and `USDe` address tokens and price feeds. The seed supply was correctly implemented as well. There was a difference between forum and IPFS, informed `ACI`.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
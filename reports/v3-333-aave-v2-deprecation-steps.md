# Proposal 333. Aave v2 non-Ethereum pools next deprecation steps

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=333)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-aave-v2-non-ethereum-pools-next-deprecation-steps/22445)

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0x37018B59345155e460B9D395E17A72844C0708aF)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xD4Db131943Ca1A93bDD626133053bdf274762770)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Proposal to progress on the deprecation of the lowest-size Aave v2 pools (Polygon and Avalanche v2), by freezing all the assets, not allowing more growth on both pools, while same time being non-invasive for users (they can withdraw, repay, and migrate to v3).

### Proposal Creation
Transaction: [0xe677cc41d46027434c3d8eb9a88dd69c7693f6cd8d09e3ae362ddfee87fe645d](https://etherscan.io/tx/0xe677cc41d46027434c3d8eb9a88dd69c7693f6cd8d09e3ae362ddfee87fe645d)
- `proposalId`: 333
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x7b1181d262f200903779ee948722340d1c9ecd57c7aa82fb7139ad4317c97de7

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 116,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 85,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x7b1181d262f200903779ee948722340d1c9ecd57c7aa82fb7139ad4317c97de7",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/333.md)

**Payload Reports**

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/116.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/85.md)


### Technical Analysis
The assets which were modified are the correct assets that were mentioned in the IPFS and forum 
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
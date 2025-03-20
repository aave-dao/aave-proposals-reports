# Proposal 272. Gov v3 VotingMachine / VotingPortal maintenance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=272)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/71)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xc15C40D0fb00672152499fa9CDFDC4AF14F31dC8)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x01FE626182E8f3FB5549919C9923061536eba58B)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xd092B902B3B11CeC912C7CC661316E07b509B6f5)



## Certora Analysis

### Proposal Types
* :scroll: :small_red_triangle: Contract upgrades


### Context
Proposal to make minor improvements on the Governance v3 VotingMachine smart contracts.

After more than 1 year of working in production without changes, the Aave governance v3 Voting Machine smart contracts (Ethereum, Polygon, Avalanche) require minor maintenance to move them to an up-to-date state with the rest of the system, more precisely the a.DI (Aave Delivery Infrastructure) directly connected.

As they are not upgradeable, it is necessary to deploy new DataWarehouse contracts, new VotingStrategy contracts and new VotingPortals.

### Proposal Creation
Transaction: [0x29316c9421f44c2ed7a8f69d00d21dc0f9785cbe92aecd1bc83d55adb0a2ba4c](https://etherscan.io/tx/0x29316c9421f44c2ed7a8f69d00d21dc0f9785cbe92aecd1bc83d55adb0a2ba4c)
- `proposalId`: 272
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xc5e038044cd09bdb8aa05b27a480f3fcb0971932bb709b6ffcca8cfe4728c0d3

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 260,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 105,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 73,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xc5e038044cd09bdb8aa05b27a480f3fcb0971932bb709b6ffcca8cfe4728c0d3",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/272.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/260.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/105.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/73.md)


### Technical Analysis
We have reviewed this maintenance upgrade and concluded that there is no issues with it.


### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
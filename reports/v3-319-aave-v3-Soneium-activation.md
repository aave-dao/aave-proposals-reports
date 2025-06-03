# Proposal 319. Aave V3.3 Soneium Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=319)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-deploy-aave-on-soneium/21204/9)

### Payloads



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking

* :gem: :new: Listing new assets


### Context
This proposal allows the Aave governance to activate the Aave V3 Soneium pool (3.3) by completing all the initial setup and listing USDCe, USDT, WETH as suggested by the risk service providers engaged with the DAO on the governance forum.

All the Aave Soneium V3 addresses can be found in the [aave-address-book](https://github.com/bgd-labs/aave-address-book/blob/18ac617a151d271c9c41d3565c8e4422d1fc6e18/src/AaveV3Soneium.sol).


### Proposal Creation
Transaction: [0x6f448a9f204fbe88e345a811b195d8a4393996fc6fd2191483524a8c918b13e6](https://etherscan.io/tx/0x6f448a9f204fbe88e345a811b195d8a4393996fc6fd2191483524a8c918b13e6)
- `proposalId`: 319
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x44f824083cacc5f681288b9868340d1a3164fa238efbd4f442003cb0ca6d0962

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1868",
            payloads_controller: "0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf",
            payload_id: 1,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x44f824083cacc5f681288b9868340d1a3164fa238efbd4f442003cb0ca6d0962",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/319.md)

**Payload Reports**


### Technical Analysis

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
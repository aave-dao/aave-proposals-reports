# Proposal 330. Enable additional SVR oracles

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=330)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-aave-chainlink-svr-v1-activation-phase-3/22387)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x32AE8876FcCe653995388E835e41e5AC9E1ecC70)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Activates SVR feeds for ETH correlated assets and USDC on Aave V3 Ethereum core.

### Proposal Creation
Transaction: [0xf92dbc6512a000cce4366a85ae5e3f4b8fe954f8532011d13cbfb44d0935f8b4](https://etherscan.io/tx/0xf92dbc6512a000cce4366a85ae5e3f4b8fe954f8532011d13cbfb44d0935f8b4)
- `proposalId`: 330
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xbf3732c30fd9456b77d74fac07d4fe0ce84374d712e58f5338d16a9f2dea994c

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 307,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xbf3732c30fd9456b77d74fac07d4fe0ce84374d712e58f5338d16a9f2dea994c",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/330.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/307.md)


### Technical Analysis

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
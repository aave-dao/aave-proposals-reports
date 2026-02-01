# Proposal 442. Listing PT Ethena May

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=442)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-usde-susde-may-expiry-pt-tokens-on-aave-v3-core-instance/23882)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xe46856e90Ec2BDb06C1Ff07b842b93d00484e597)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets


### Context
We propose onboarding the USDe and sUSDe May-expiry PT tokens to the Aave V3 Core instance.  
The previously onboarded USDe and sUSDe PT tokens have brought significant inflows to Aave. In preparation for their expiry and rollover, we propose onboarding the next expiry of these PT tokens. We expect deposits to at least match those of the current-expiry PT tokens, with the potential for additional sidelined demand.

### Proposal Creation
Transaction: [0x5433d1b6a3b6c163ae5a52c85b1d0640ab978a6ced3bd7c4141a8a0dd725b7c6](https://etherscan.io/tx/0x5433d1b6a3b6c163ae5a52c85b1d0640ab978a6ced3bd7c4141a8a0dd725b7c6)
- `proposalId`: 442
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xd996400425ba4dd6835d8abf7ee8db7519c9a21d40295cd9912035de2000178c

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 399,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xd996400425ba4dd6835d8abf7ee8db7519c9a21d40295cd9912035de2000178c",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/442.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/399.md)


### Technical Analysis

We have checked the alignment of risk parameters between the Forum, IPFS, and the payload.

We have verified oracle addresses and expiry.

We have verified that `0xac140648435d03f784879cd789130F22Ef588Fcd` is set as the emission admin for both PTs.

We have checked that the `COLLECTOR` has a sufficient amount of both tokens to fund the `EXECUTOR_LVL_1`.

We have verified that the setup on the `AGENT_HUB` is correct.

The proposal is consistent with the descriptions on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
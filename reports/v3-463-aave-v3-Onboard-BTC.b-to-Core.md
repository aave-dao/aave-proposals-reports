# Proposal 463. Onboard BTC.b to Aave V3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=463)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-btc-b-to-aave-v3-core-instance/23357)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xA0c95B15A0E8EAc5D09f45E73b71b2F78AB48a57)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :gem: :new: Listing new assets


### Context
This proposal seeks to onboard BTC.b to the Aave V3 deployment on the Core Instance.

As the onboarding of BTC.b has already been approved and executed on the Avalanche Aave V3 instance, this proposal follows the Direct-to-AIP path to extend BTC.b support to the Core instance.

### Proposal Creation
Transaction: [0xd1a1c79a69963c6040426f2aecb997eb53424c448675a0e739b1d3ceb9957b64](https://etherscan.io/tx/0xd1a1c79a69963c6040426f2aecb997eb53424c448675a0e739b1d3ceb9957b64)
- `proposalId`: 463
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x8abd16009e30b7740e502d84ec964d03a4e10bc99f31cbd34abd5d02d443c82b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 421,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x8abd16009e30b7740e502d84ec964d03a4e10bc99f31cbd34abd5d02d443c82b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/463.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/421.md)


### Technical Analysis

We confirmed the new listing of `BTC.b` with the correct risk params.

We have verified seed amounts with respect to decimal precision.

We confirmed the assignment of the Emission Admin role to the ACI (`0xac140648435d03f784879cd789130F22Ef588Fcd`) for the underlying, `aToken`, and `vToken`. 

We have verified proposal logic and validate its execution via seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
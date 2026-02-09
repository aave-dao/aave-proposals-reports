# Proposal 444. Onboard Strata srUSDe PT tokens to V3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=444)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-strata-srusde-pt-tokens-to-v3-core-instance/23481)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xC5D3ffC14c15C553411961576B475Eb9fB0B75B8)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets


### Context
This proposal seeks to onboard the Strata srUSDe PT tokens to the Aave V3 Core Instance. This specific AIP is onboarding the April expiry PT token.

### Proposal Creation
Transaction: [0x6730a82c8c8f6761c7e49f6533cef683c7f970a29bc9e114143ea85beac3f44f](https://etherscan.io/tx/0x6730a82c8c8f6761c7e49f6533cef683c7f970a29bc9e114143ea85beac3f44f)
- `proposalId`: 444
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x4c5ae8b97620b88e0da6da0fde99dad21b121fac07165ac15b80c865da16bcae

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 400,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x4c5ae8b97620b88e0da6da0fde99dad21b121fac07165ac15b80c865da16bcae",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/444.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/400.md)


### Technical Analysis

We checked alignment between the governance forum, IPFS, and the payload.  
We found some discrepancies and brought them to ACI’s attention. These can be updated later, so we approved the proposal.  
We verified seed amounts with respect to decimal precision.  
We checked price feed addresses.
We verified risk parameters.  
We validated the proposal logic and verified execution via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 448. Update syrupUSDC liquidation protocol fee

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=448)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-update-syrupusdc-liquidation-protocol-fee-on-aave-v3-base-instance/23963)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x12Ce6F6c44bfD860ccc143aDA41ccB9d68A973ED)

* Base - [proposal payloads](https://basescan.org/address/0x4d4f6dAAddc5a98c5cb3ffd732c035d389741eaB)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This Direct to AIP proposal plans to update SyrupUSDC config and add a 10% Liquidation Protocol Fee on Aave V3 Base Instance.

Update the Liquidation Protocol Fee from 0% to 10% for SyrupUSDC on Aave V3 Base Instance.  
We will also batch with this AIP a correction of last PT srUSDe e-mode labels.


### Proposal Creation
Transaction: [0x0231fd91baffdeaa9481b2d3253bb30a04d53cd3db10bfc58579380adaf50136](https://etherscan.io/tx/0x0231fd91baffdeaa9481b2d3253bb30a04d53cd3db10bfc58579380adaf50136)
- `proposalId`: 448
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x3d5eedc48f92c9cf506a621cf50a3cfb2b7f6273fd5f19ed71b415f98a3b58b2

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 403,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 98,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x3d5eedc48f92c9cf506a621cf50a3cfb2b7f6273fd5f19ed71b415f98a3b58b2",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/448.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/403.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/98.md)


### Technical Analysis

We have verified the update of the relevant E-Mode labels.  
We have validated that the liquidation protocol fee for `SyrupUSDC` changed from 0% to 10%.


The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
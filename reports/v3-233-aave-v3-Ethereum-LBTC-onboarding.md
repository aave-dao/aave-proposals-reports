# Proposal 233. Onboard LBTC & Enable LBTC/WBTC liquid E-Mode

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=233)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-enable-lbtc-wbtc-liquid-e-mode-on-aave-v3-core-instance/20142)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x76182E201EeCD702253A12B3fEECDF98fCdBf724)


## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets

### Context
This proposal aims to onboard LBTC and enable LBTC/WBTC liquid E-Mode for the Main Instance. By implementing this change, we seek to enhance capital efficiency for borrowers using LBTC/WBTC as collateral.

### Proposal Creation
Transaction: [0x7089ce36fdc6e7a1fcc472e6a1b83fc586043665897ec2f600f09582e2efb755](https://etherscan.io/tx/0x7089ce36fdc6e7a1fcc472e6a1b83fc586043665897ec2f600f09582e2efb755)
- `proposalId`: 233
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x9ec4e2279298c5947f6ec44993ef77a53517a1ea0f2d0458c147079a83f2413f

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 234,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x9ec4e2279298c5947f6ec44993ef77a53517a1ea0f2d0458c147079a83f2413f",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/233.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/234.md)


### Technical Analysis
We have verified that the listed risk parameters are identical to the IPFS and forum. Given BGD review, the emode LT + liquidation bonus and max slashable configuration to 10% its safe to use the BTC/USD price feed instead of a dedicated LBTC\BTC feed. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
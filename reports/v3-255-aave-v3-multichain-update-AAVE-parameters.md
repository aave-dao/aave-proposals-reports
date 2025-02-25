# Proposal 255. Update AAVE Token LTV/Liquidation Percentages

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=255)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-update-aave-token-ltv-liquidation-percentages/20973)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9a8DBD9891a48e49DB068B79518160d286a34967)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x52241733E2F2CA8BF31c4b5dA499146882B19a54)



## Certora Analysis

### Proposal Types
* :wrench: :bar_chart: Configuration updates

### Context
Following recent meaningful growth in liquidity and market cap of AAVE token, the risk parameters of the token as collateral are adjusted to values of asset with similar risk profile.

### Proposal Creation
Transaction: [0xebf2b1816a5ad7477d7e5bb4e0db579b3c9634238179bcca16709d074c381af4](https://etherscan.io/tx/0xebf2b1816a5ad7477d7e5bb4e0db579b3c9634238179bcca16709d074c381af4)
- `proposalId`: 255
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x3ad0eab265e54bfe5a6b27fcffc917a948886394c88033c06bcb77e737accc3d

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 250,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 76,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x3ad0eab265e54bfe5a6b27fcffc917a948886394c88033c06bcb77e737accc3d",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/255.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/250.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/76.md)


### Technical Analysis
We verified that the proposal adjust only the AAVE token collateralization parameters, and solely on Ethereum and Arbitrum. The values were adjusted exactly to the values specified in the proposal description.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 225. Remove USDS from sUSDe Liquid E-Mode

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=225)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-proposal-to-remove-usds-from-susde-liquid-e-mode-in-aave-prime-instance/20264)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x398F224889e8b65a7d5BF25474cEf2aeca4dD97A)

* Ethereum Lido - [proposal payloads](https://etherscan.io/address/0xbdc315e7Ec5DCc4cCF4189B3E7bb9691c51Fb39b)


## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
This proposal recommends the removal of USDS from the sUSDe Liquid E-Mode in the Aave Prime instance.

### Proposal Creation
Transaction: [0xe108608cf4aedf0d16e951a55c9c8e07f1f39667d3cf7c560c6723840c2e7a91](https://etherscan.io/tx/0xe108608cf4aedf0d16e951a55c9c8e07f1f39667d3cf7c560c6723840c2e7a91)
- `proposalId`: 225
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x63789665d092c33439ca04f323667f770156b3a16123712bb63982c2912f8fa9

**`createProposal()` Parameters**
```
{
    "payloads": [
        {
            "chain": "1",
            "accessLevel": 1,
            "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            "payloadId": 228
        }
    ],
    "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    "ipfsHash": "0x63789665d092c33439ca04f323667f770156b3a16123712bb63982c2912f8fa9"
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/225.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/228.md)

* Ethereum Lido - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/228.md)


### Technical Analysis
The technical adjustments outlined in the proposal have been successfully implemented. USDS has been correctly removed from the sUSDe Liquid E-Mode on the Aave Prime instance, and the liquidation bonus has been updated to 4% on both the Core and Prime instances. Verification confirms proper parameter updates and alignment with the protocol’s risk management framework.


The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
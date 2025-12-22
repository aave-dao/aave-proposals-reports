# Proposal 421. Remove USDS as collateral and increase RF across all Aave Instances

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=421)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-remove-usds-as-collateral-and-increase-rf-across-all-aave-instances/23426)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x281ECdaB4013A227f3119863ae73028339db550A)

* Ethereum 2 - [proposal payloads](https://etherscan.io/address/0x7d94c5a772a4DDeB9a488E7999ADb464764754C5)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x903114b04a125810A85773070eB5A0FC4aE45975)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xC7e0439CB187a9d1A8736E830e43Cce3C76CE8C1)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x3aF1411fd577f78144E867F875b86e3Ed200c2Ab)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xcd5B813d7981270989e85ef779Bb5608AB4ac712)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x9F518ED1C6Fb675d67828C8F4876c3e90BF65b77)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
This AIP proposes removing USDS as collateral and increasing RF across all Aave instances.
USDS generates negligible revenue while its issuance model introduces asymmetric risks that could impact Aave’s stability.



### Proposal Creation
Transaction: [0x4ba0338d319607b7d9aa9d3052016a91cf15fc29383c8bfe7cc20fed74d373fa](https://etherscan.io/tx/0x4ba0338d319607b7d9aa9d3052016a91cf15fc29383c8bfe7cc20fed74d373fa)
- `proposalId`: 421
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x8145d5e782e1649757a7e035620c0ce53b93cd066eface7f4b1f774e1500cfef

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 381,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 135,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 103,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 90,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 107,
        },
        {
            chain: "1088",
            payloads_controller: "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            payload_id: 45,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x8145d5e782e1649757a7e035620c0ce53b93cd066eface7f4b1f774e1500cfef",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/421.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/381.md)

* Ethereum 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/381.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/135.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/103.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/90.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/107.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/45.md)


### Technical Analysis
We have confirmed alignment between the forum, IPFS, and the payloads. On Ethereum Core and Prime, we have verified that USDS is being disabled from all E-Mode categories. We have validated all updated supply and borrow caps. We have reviewed the payload logic and validated execution via Seatbelt. The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
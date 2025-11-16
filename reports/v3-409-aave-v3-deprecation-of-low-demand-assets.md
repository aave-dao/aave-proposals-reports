# Proposal 409. Deprecation of Low Demand Volatile Assets on Aave V3 Instances

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=409)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-deprecation-of-low-demand-volatile-assets-on-aave-v3-instances/23261)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x56C478c8C8301F9FbD6BB335DA50089b4abcD2eB)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x2c8AEA70D7887F9306F275C0E1f37F2082129D5F)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0xb9ce69Ca5e716A8dBe71e246ae71c8d7a0aB621A)

* zkSync Era - [proposal payloads](https://era.zksync.network/address/0x97932F88E48DaB2510C154cDa7a5b905c8E7515F)



## Certora Analysis

### Proposal Types

:wrench: :bar_chart: Configuration updates


### Context
This AIP is the second phase of the deprecation of low-demand assets proposed by Chaos Labs. Following the recent market volatility and oracle desynchronization, which exposed certain assets to heightened systemic risk, the proposal recommends setting the LTV of selected assets to 0% and disabling their borrowability. These measures aim to mitigate volatility-related risks and preserve Aave’s protocol stability while phasing out underutilized assets with minimal revenue contribution.

### Proposal Creation
Transaction: [0x4fb17d8bb80a38ef136f6aea42a972dd5e6f13e52ca93bbc0beb46351aa86e80](https://etherscan.io/tx/0x4fb17d8bb80a38ef136f6aea42a972dd5e6f13e52ca93bbc0beb46351aa86e80)
- `proposalId`: 409
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x4cc9da7ec6a32cbd5571aedb4212b5d34af8888d2bfca14145362439a0b553cc

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 370,
        },
        {
            chain: "1088",
            payloads_controller: "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            payload_id: 43,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 50,
        },
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 32,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x4cc9da7ec6a32cbd5571aedb4212b5d34af8888d2bfca14145362439a0b553cc",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/409.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/370.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/43.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/50.md)

* zkSync Era - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/32.md)


### Technical Analysis
We have confirmed alignment between the forum post, the IPFS content, and the on-chain payload.
We were concerned about potential griefing attack and contacted `ACI` and they have confirmed that its ok and we agreed. 
We have validate assets addresses and the payload's logic and we confirm that the payload will execute as intended. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
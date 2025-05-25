# Proposal 313. Configuration maintenance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=313)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/86)

### Payloads

* Ethereum Core - [proposal payloads](https://etherscan.io/address/0xf791278c12a20F29967ea11ea5eCA384a461A72d)

* Ethereum Prime - [proposal payloads](https://etherscan.io/address/0x6e6c006bD2B0bE4d2FACEBC02Cef4832F4625661)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x95DF7C254c338209ebE4c7FEd146148dA644d7C2)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x55aCfdAf71a67bf201df8A1c96d3Ae114bD7c6DC)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x6547f78FEE9B59a2CA116b95dBE684cBbd6409e1)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x26f13CFBC576eC58003B1270b0323F4a7bF50dBE)

* Base - [proposal payloads](https://basescan.org/address/0x8355C690542f0d7A9505f010ac0669Df71268Ab9)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x00e7478a5b15B04DD2fc12ee2Be0f4587e1502B7)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x0808604a5A1f829087271be6b80c67fE2074C342)

* zkSync Era - [proposal payloads](https://era.zksync.network/address/0x36614CF47aF50Af6f5c4d370170aC15d4b86c354)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal aims to fix inconsistent / suboptimal configurations across various pools. 

### Proposal Creation
Transaction: [0xbf626e34f0ce88240bf40eeff910187c03f622d44114d91dc21a8557a78b4ce1](https://etherscan.io/tx/0xbf626e34f0ce88240bf40eeff910187c03f622d44114d91dc21a8557a78b4ce1)
- `proposalId`: 313
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x1bd0bf584240ed9572b23d3547b891fadefd0909a1c79bf5ba08aa370c71bc61

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 289,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 111,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 78,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 75,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 88,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 70,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 52,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 41,
        },
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 24,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x1bd0bf584240ed9572b23d3547b891fadefd0909a1c79bf5ba08aa370c71bc61",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/313.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/289.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/111.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/78.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/75.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/88.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/70.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/52.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/41.md)

* zkSync Era - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/24.md)


### Technical Analysis
We have validated the correct assets have been modified.
 
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 334. Upgrade Aave instances to v3.4

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=334)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-bgd-aave-v3-4/21572/21)

### Payloads

* Ethereum 1 - [proposal payloads](https://etherscan.io/address/0xC2584B9cA7759FE1ac48D8aE38aeAFE12dbC9876)

* Ethereum 2 - [proposal payloads](https://etherscan.io/address/0x028229cdAADa074A17980B4d69A1483a738D24cA)

* Ethereum 3  - [proposal payloads](https://etherscan.io/address/0x1FaaB253f2cb5462eac72BCE7a379D3fc5A17E10)

* Ethereum 4 - [proposal payloads](https://etherscan.io/address/0x132d178557a0c0e6354762542eC1bc73EbB79549)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x864fe2B34b6066e3D14FC1FB460Faf2B1b069d64)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xcD21f2532d3c8AcAACC5217F50d5be4F611bbC12)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0xB8a29caf8Cd73Db3CDA8f294b2a0d2933C2fc62f)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x8B5Ff77430E2c7e5f46ACD1318c0b5b5d43ef379)

* Metis - [proposal payloads](https://explorer.metis.io/address/0xf527fF293EA12320E5246B2668937D0A694EA46D)

* Base - [proposal payloads](https://basescan.org/address/0x41d7188B68A6b334071DB5A1D33Ce4b9109899B3)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x6f6A25C4D03EdA3800863522d1340954021046F5)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x5914AB024e4D730886ad2f2aF8790C466b0c2868)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0xFA6a2793c50fD498ff8d53510d6EFfB66C7A03C4)

* zkSync Era - [proposal payloads](https://era.zksync.network/address/0xE7dBD6023B9c7eD90f65CE61458B7b4A5c22A1Fa)

* Linea - [proposal payloads](https://lineascan.build//0xe3DE4BA75c667b86FC82f4C0Db0aF83Dd9626346)

* Celo - [proposal payloads](https://celo.blockscout.com//0x1E2a398AAe0FF798953603f774aC1143EA0ba545)

* Sonic - [proposal payloads](https://sonicscan.org/address/0xF90c3AB36F17574F2A490e9D98b0B5301332BBFa)

* Soneium - [proposal payloads](https://soneium.blockscout.com/address/0x334bA9f803e77Fb68c4849d6C51345af2D563Ff7)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades


### Context
Upgrade the Aave v3 Protocol across all networks from v3.3 to v3.4.

### Proposal Creation
Transaction: [0x4d99696fe18ac2f78d3ae18c9d61cfa705c74ab58bd52534ad34c0ee131237d3](https://etherscan.io/tx/0x4d99696fe18ac2f78d3ae18c9d61cfa705c74ab58bd52534ad34c0ee131237d3)
- `proposalId`: 334
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x7915e4e3667981f3a6a34695c8693fdc455f26d128c67e52e18ef56d09ad941d

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 301,
        },
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 302,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 114,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 81,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 77,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 90,
        },
        {
            chain: "1088",
            payloads_controller: "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            payload_id: 40,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 73,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 54,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 43,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 40,
        },
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 28,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 9,
        },
        {
            chain: "42220",
            payloads_controller: "0xE48E10834C04E394A04BF22a565D063D40b9FA42",
            payload_id: 6,
        },
        {
            chain: "146",
            payloads_controller: "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695",
            payload_id: 4,
        },
        {
            chain: "1868",
            payloads_controller: "0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf",
            payload_id: 2,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x7915e4e3667981f3a6a34695c8693fdc455f26d128c67e52e18ef56d09ad941d",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/334.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/301.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/114.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/81.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/77.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/90.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/40.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/73.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/54.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/43.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/40.md)

* zkSync Era - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/28.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/9.md)

* Celo - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42220/0xE48E10834C04E394A04BF22a565D063D40b9FA42/6.md)


### Technical Analysis
In addition to the audit conducted prior to the upload of the AIP, we performed an additional technical review of the proposal. This included a thorough inspection of the AIP logic to ensure correctness and alignment with protocol expectations. We checked for unintentional reverts and other potential failure points. A detailed comparison was made between the proposed code and the live version to confirm the scope and integrity of the changes. Additionally, we reviewed the Seatbelt.

For reference, the full audit report conducted by Certora prior to the AIP upload can be found [here](https://github.com/aave-dao/aave-v3-origin/blob/74412e2b6e0b1973fac6837b6a488f8eaaeac4b1/audits/2025-06-11_Certora_Aave-v3.4_Report.pdf).

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
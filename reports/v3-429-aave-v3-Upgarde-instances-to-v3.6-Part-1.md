# Proposal 428. Upgrade Aave instances to v3.6 Part 1

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=429)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-bgd-aave-v3-6/23172/4)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x46738047c72952953b14e9801648EF05F056EA2C)

* Ethereum - [proposal payloads](https://etherscan.io/address/0x000a26DE3Ac9d5Fa08E4DaF924521b5910224eAb)

* Optimisim - [proposal payloads](https://optimistic.etherscan.io/address/0x2957a5b8b4A5fC6Cf9Fe5b2D79B66a18871abb20)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x1B72B5799B455bAf19Af89495B5d35C155956587)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x073264F6F30f8a50189E144967B7f22a6D22003f)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x0a4C8f5740c9e21d64484Ccfcd85a2FeaDC004d5)

* ZkSync - [proposal payloads](https://era.zksync.network/address/0xA485DE0D7D43B2b47731ae436daa1de32033fC12)

* Celo - [proposal payloads](https://celoscan.io/address/0x0A2b39388E7B716da882DcDAB6080F57f9a8B9a1)

* Sonic - [proposal payloads](https://sonicscan.org/address/0x1306a50626B475ae21dB7210356BdDE1EAA2781a)

* Soneium - [proposal payloads](https://soneium.blockscout.com/address/0x7ada3b2963342ce5417f31f82e0eFfa8E1494350)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades



### Context
#### Simple Summary
Upgrade the Aave protocol instances from v3.5 to v3.6 Part 1.

#### Motivation
Aave v3.6 enhances isolation, via more fine-grained configurations and the decoupling of eMode and eMode0 settings. For a comprehensive overview of the changes, please refer to the documentation.

### Proposal Creation
Transaction: [0x22f578766cc50ddf9fb04329746c1f2fd16c850df9bf79aaaba15518a1d3524a](https://etherscan.io/tx/0x22f578766cc50ddf9fb04329746c1f2fd16c850df9bf79aaaba15518a1d3524a)
- `proposalId`: 429
- `creator`: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- `accessLevel`: 1
- `ipfsHash`: 0xae1c2adc47d96ea7c9a5e3a6a68ec9e92c6e96ba1d146d97dffbbcb6f91a7b1f

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "389" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "89" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "44" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "67" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "48" 
    }, 
    { 
      "chain": "324", 
      "accessLevel": "1", 
      "payloadsController": "0x2E79349c3F5e4751E87b966812C9E65E805996F1", 
      "payloadId": "33" 
    }, 
    { 
      "chain": "42220", 
      "accessLevel": "1", 
      "payloadsController": "0xE48E10834C04E394A04BF22a565D063D40b9FA42", 
      "payloadId": "9" 
    }, 
    { 
      "chain": "146", 
      "accessLevel": "1", 
      "payloadsController": "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695", 
      "payloadId": "12" 
    }, 
    { 
      "chain": "1868", 
      "accessLevel": "1", 
      "payloadsController": "0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf", 
      "payloadId": "4" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0xae1c2adc47d96ea7c9a5e3a6a68ec9e92c6e96ba1d146d97dffbbcb6f91a7b1f" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/389.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/389.md)


* Optimisim - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/89.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/44.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/67.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/48.md)

* ZkSync - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/33.md)

* Celo - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42220/0xE48E10834C04E394A04BF22a565D063D40b9FA42/9.md)

* Sonic - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/146/0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695/12.md)

* Soneium - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1868/0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf/4.md)


### Technical Analysis

We have verified transfer addresses and amounts with respect to decimal precision and validated via Seatbelt for both CERTORA and BGD.

We have validate that all `POOL_ADDRESSES_PROVIDER`  values match `IPool(params.poolImpl).ADDRESSES_PROVIDER()` 

We have checked that the provided pools match the `AToken` & `VToken` Pools.

We have verified the payload logic and execution.
E-Mode LTV-zero logic was reviewed to ensure no unintended category or asset side effects.
Storage layout compatibility between previous and new implementations has been reviewed and validated.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
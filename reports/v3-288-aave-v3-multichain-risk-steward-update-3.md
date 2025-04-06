# Proposal 288. Risk Steward Parameter Updates Phase 3

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=279)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-finance-steward-deployment/21495)

### Payloads

* Ethereum Core - [proposal payloads](https://etherscan.io/address/0xC4c3C70aD09643258e5A00578e93E43B45D533d1)

* Ethereum Prime - [proposal payloads](https://etherscan.io/address/0xB60958395250A31Ddf164058b888B492Ba4Be410)

* Ethereum EtherFi - [proposal payloads](https://etherscan.io/address/0x6a7bfeB74d0e477Df13A3fa3B766Bc48e19EB3Df)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x041495220A8cF5EE374478C198F010BB98ce01E0)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xED80A788C1656dFB5742a95e5213B53d618b4603)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x3D00a3AA182D3300B06661aEA01959E834061dde)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x1FBc38147b309611Fd9B0aAE343c28efBd5d523d)

* Metis - [proposal payloads](https://explorer.metis.io/address/0xd6e5B763749EE0D52B521eDE7D0921f3220603E6)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xe4f741Ca41f7F850268fA1AE5dB4bbec05AAb593)

* Base - [proposal payloads](https://basescan.org/address/0xF7124e25Cc9069f0a648051c71184638997BFff8)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x87C34c369352229199922954e1F83d6277e76a83)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0x8ad2C870c0Bc5c9D357808f0838B00f40b11068f)

* Sonic - [proposal payloads](https://sonicscan.org//address/0x07428705De1085dcEDA1A533Ac773fe8BFe6E1F3)

* Celo - [proposal payloads](https://celoscan.io/address/0xB510C1d34ED499e17A110341379384C60a094EeE)

* zkSync - [proposal payloads](https://era.zksync.network//address/0x7Ed87645a8fD59aFda3d42651c4cf9eE9d4C792)

* Linea - [proposal payloads](https://lineascan.build//0xCD149C5143C85387213DC544f20B49Ded26Bc400)



## Certora Analysis

### Proposal Types
* :wrench: :bar_chart: Configuration updates


### Context
This publication details the initial configuration of the Aave Finance Steward PoolExposure module.

The Finance Steward role is comprised of a set of Modules (Smart Contracts) that provide approved signers with the ability to perform DAO approved actions such as swapping tokens or migrating assets from Aave V2 to Aave V3.

### Proposal Creation
Transaction: [0xe545edaf2200f226212e10a1e9e38daf75986256743ee9df80d8bfb8a0308c10](https://etherscan.io/tx/0xe545edaf2200f226212e10a1e9e38daf75986256743ee9df80d8bfb8a0308c10)
- `proposalId`: 288
- `creator`: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x0526e6e2532008aeefcc8e484045821dc5d4ae94290be1109f787a609728d310

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "265" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "107" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "75" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "72" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "84" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "37" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "48" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "65" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "40" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "37" 
    }, 
    { 
      "chain": "42220", 
      "accessLevel": "1", 
      "payloadsController": "0xE48E10834C04E394A04BF22a565D063D40b9FA42", 
      "payloadId": "3" 
    }, 
    { 
      "chain": "146", 
      "accessLevel": "1", 
      "payloadsController": "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695", 
      "payloadId": "2" 
    }, 
    { 
      "chain": "324", 
      "accessLevel": "1", 
      "payloadsController": "0x2E79349c3F5e4751E87b966812C9E65E805996F1", 
      "payloadId": "20" 
    }, 
    { 
      "chain": "59144", 
      "accessLevel": "1", 
      "payloadsController": "0x3BcE23a1363728091bc57A58a226CF2940C2e074", 
      "payloadId": "8" 
    }, 
  ], 
  "votingPortal": "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6", 
  "ipfsHash": "0x0526e6e2532008aeefcc8e484045821dc5d4ae94290be1109f787a609728d310" 
}
```



### Technical Analysis
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
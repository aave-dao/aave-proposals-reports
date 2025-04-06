# Proposal 279. Finance Steward Deployment: Pool Exposure Module

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=279)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-finance-steward-deployment/21495)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xB74a044c269D92a8a9C35D5B2828a1744F97B732)

* Ethereum 2 - [proposal payloads](https://etherscan.io/address/0x3136DB2A0838119A41259224Aac51077E100FF78)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xD3026f4fEb52Ff83Fd69BDF380b80e473cA80496)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xB0C6777bc6d14294E907868c061518cB44133597)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0xB5c3C7209BD6A7c1AA80570ADA53A66F20948483)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x82e5C99997d6f028293442759bB5DbEf67Be9114)

* Base - [proposal payloads](https://basescan.org/address/0x156db3F414a2Ef40074a486425C0bE1928C4b724)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x96612bB562B8815f46172FF1B80Df7370552AdCe)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0x2eCa30f3313567cBe79814882003adf1a07Bd168)

* Sonic - [proposal payloads](https://sonicscan.org//address/0x4f2B2Dc67C2E0C9B33b91d83108BA318D399dD9b)

* Linea - [proposal payloads](https://lineascan.build//0xB7FaE3122bB58DEbFd06130ddf74ca97c32583B0)



## Certora Analysis

### Proposal Types
* :scroll: :small_red_triangle: Contract upgrades

* :handshake: Permission granting and revoking


### Context
This publication details the initial configuration of the Aave Finance Steward PoolExposure module.

The Finance Steward role is comprised of a set of Modules (Smart Contracts) that provide approved signers with the ability to perform DAO approved actions such as swapping tokens or migrating assets from Aave V2 to Aave V3.

### Proposal Creation
Transaction: [0xb1cfef1962e598771bde4e505aee35681f34c861596cdddeeddc38a8657b52fa](https://etherscan.io/tx/0xb1cfef1962e598771bde4e505aee35681f34c861596cdddeeddc38a8657b52fa)
- `proposalId`: 279
- `creator`: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x0b0274c64c3044960cc136a5c813bb461e40da836c5873e85f99aafd1cd9f813

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "263" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "106" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "74" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "71" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "83" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "64" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "38" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "36" 
    }, 
    { 
      "chain": "59144", 
      "accessLevel": "1", 
      "payloadsController": "0x3BcE23a1363728091bc57A58a226CF2940C2e074", 
      "payloadId": "6" 
    }, 
    { 
      "chain": "146", 
      "accessLevel": "1", 
      "payloadsController": "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695", 
      "payloadId": "1" 
    }, 
  ], 
  "votingPortal": "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6", 
  "ipfsHash": "0x0b0274c64c3044960cc136a5c813bb461e40da836c5873e85f99aafd1cd9f813" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/279.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/263.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/106.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/74.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/71.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/83.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/64.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/38.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/36.md)

* Sonic - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/146/0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695/1.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/6.md)


### Technical Analysis
We have reviewed the steward, confirmed all intended instances has been onboarded. We checked the dust bin supplied with the correct amounts.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
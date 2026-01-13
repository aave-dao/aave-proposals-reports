# Proposal 433. Upgrade Aave instances to v3.6 Part 2

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=433)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-bgd-aave-v3-6/23172/4)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xaCAeFE6Cf2ef667fA8Be03AaeDe402CBcD6ed44D)
* Ethereum - [proposal payloads](https://etherscan.io/address/0x95D6cDe855d58DEA260e1A8297E299176FC11b6f)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x4e4BaA9cbD2FF6281F5bA050810F061A4E6e0850)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0xF045F5E209Bc758a85aE75f5e2e79fDC50fD499f)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xb8FD4Fe11aa830EEC7f73FD5435366052665Eda5)

* Base - [proposal payloads](https://basescan.org/address/0x3D7a80B4c666FB285ca49f145F8467FaA80dB301)

* BnB - [proposal payloads](https://bscscan.com/address/0x4a61666015eC3bf05b9CC7754F8A475833d160dF)

* Linea - [proposal payloads](https://lineascan.build/address/0xef45332E99700297e813F0E236E14a48A4CfAC99)

* Plasma - [proposal payloads](https://plasmascan.to/address/0x23cEfa65515274C5832F1D4F789E1d27b301e1E6)




## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades



### Context
#### Simple Summary
Upgrade the Aave protocol instances from v3.5 to v3.6 Part 2.  
The upgrade payload updates the implementations of the Pool, PoolConfigurator, AToken & VariableDebtToken on the second set of pools, namely Mainnet(Core), Mainnet(Prime), Plasma, Base, Arbitrum, Avalanche, Linea, BNB Chain, Polygon.

On mainnet core the payloads varies slightly to account for:  

aAave which has a different implementation due to the governance delegation integration
vGHO which has a different implementation due to the deprecated discount mechanism on stkAAVE


### Proposal Creation
Transaction: [0x3606be3deabd151ac4197175a6c6f7dc3e0288162f8f184d6dd31b1c0baca0d7](https://etherscan.io/tx/0x3606be3deabd151ac4197175a6c6f7dc3e0288162f8f184d6dd31b1c0baca0d7)
- `proposalId`: 433
- `creator`: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- `accessLevel`: 1
- `ipfsHash`: 0x39a6a154b425a4ab0f51aad675c6801cc1b31e8f26680628018c0f034545a9ed

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "392" 
    }, 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "393" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "134" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "102" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "106" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "90" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "52" 
    }, 
    { 
      "chain": "59144", 
      "accessLevel": "1", 
      "payloadsController": "0x3BcE23a1363728091bc57A58a226CF2940C2e074", 
      "payloadId": "18" 
    }, 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "10" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0x39a6a154b425a4ab0f51aad675c6801cc1b31e8f26680628018c0f034545a9ed" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/392.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/392.md)

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/393.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/134.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/102.md)

* Arbitrum - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/106.md)

* Base - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/90.md)

* BnB - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/52.md)

* Linea - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/18.md)

* Plasma - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/10.md)


### Technical Analysis

We have validate that all `POOL_ADDRESSES_PROVIDER`  values match `IPool(params.poolImpl).ADDRESSES_PROVIDER()` 

We have checked that the provided pools match the `AToken` & `VToken` Pools. (Also for `A_TOKEN_WITH_DELEGATION_IMPL` &  `V_TOKEN_GHO_IMPL`)

For `UpgradePayloadMainnetCore` We have also verified that:
 - `aAAVE` new implementation is `A_TOKEN_WITH_DELEGATION_IMPL`.
 - `vGHO` new implementation is `V_TOKEN_GHO_IMPL`

We have verified the payloads logic and execution.  
E-Mode LTV-zero logic was reviewed to ensure no unintended category or asset side effects.  
Storage layout compatibility between previous and new implementations has been reviewed and validated.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
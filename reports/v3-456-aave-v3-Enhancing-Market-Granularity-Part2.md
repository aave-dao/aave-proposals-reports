# Proposal 456. Enhancing Market Granularity in Aave 3.6: part 2

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=456)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-enhancing-market-granularity-in-aave-v3-6-restricting-borrowability-and-collateralization-outside-of-liquid-emodes/23592)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x54D376E5D4f1f13A80A7F755C47b0b646b7a04a8)

* Ethereum - [proposal payloads](https://etherscan.io/address/0x8ee95C5bEFd3b8d23feB2135C4dd6138fd9A1A40)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x9ED05d839F4a4b43b8569594aa064445779F55D7)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0x491563E420226fc290bbE3CD378CEE35ffd2FC9b)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x0660eA4905eA05E336F510C595d21C3136aCeC48)

* Base - [proposal payloads](https://basescan.org/address/0x13D6276dC12a8c094058c93Eddfc2dCDa5f76c32)

* BnB - [proposal payloads](https://bscscan.com/address/0xC61708E3928536b69cc23Aa747070390f48FD3dE)

* Linea - [proposal payloads](https://lineascan.build/address/0xFfA518A7E1F48A2E8514a3B051C0Dc39627C7141)

* Plasma - [proposal payloads](https://plasmascan.to/address/0x9Fb3F5Ef9eF8D5E393cC5CeA75eB0De632076577)



## Certora Analysis

### Proposal Types


* :wrench: :bar_chart: Configuration updates

### Context
This proposal leverages the configurability improvements introduced in Aave v3.6 to strengthen risk isolation and improve parameter clarity. Specifically, it introduces:

LTV0 for assets not intended to serve as collateral outside of eModes.
Non-borrowable status for assets whose use cases are restricted to within their respective eModes.
Exclusive eMode participation, ensuring these assets are only active within targeted, high-correlation environments.
This aims to reduce systemic exposure, simplify risk management, and enable cleaner differentiation between general market assets and those intended for correlated or high-efficiency lending environments.

This AIP covers only the instances that were upgraded in part 2 and 3 of the 3.6 upgrade.

### Proposal Creation
Transaction: [0xbf456b95fbaa32afcba64e92fd3e603b533e69e2c3415fefb0fed051cc2d8e97](https://etherscan.io/tx/0xbf456b95fbaa32afcba64e92fd3e603b533e69e2c3415fefb0fed051cc2d8e97)
- `proposalId`: 456
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xe9be07adccfe26198c25f3783e6733f50a641e8dec6217d2458d8be38c406883

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "411" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "139" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "109" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "113" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "100" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "55" 
    }, 
    { 
      "chain": "59144", 
      "accessLevel": "1", 
      "payloadsController": "0x3BcE23a1363728091bc57A58a226CF2940C2e074", 
      "payloadId": "22" 
    }, 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "19" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0xe9be07adccfe26198c25f3783e6733f50a641e8dec6217d2458d8be38c406883" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/456.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/411.md)

* Polygon - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/139.md)

* Avalanche - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/109.md)

* Arbitrum - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/113.md)

* Base - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/100.md)

* BnB - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/55.md)

* Linea - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/22.md)

* Plasma - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/19.md)


### Technical Analysis

We have verified that all the specified asset statuses were updated correctly using `borrowsUpdates` and `collateralsUpdates`. Some assets were listed in the IPFS but not in the payload, but after checking, their status had already been updated.

We have checked that all new `E-Modes` have been set correctly with the correct parameters.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
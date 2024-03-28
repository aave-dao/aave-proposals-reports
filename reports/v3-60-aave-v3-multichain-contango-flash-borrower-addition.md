# Proposal 60. Contango FlashBorrower.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=60](https://vote.onaave.com/proposal/?proposalId=60)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-contango-protocol-cian-protocol-and-index-coop-to-flashborrowers-on-aave-v3/16478](https://governance.aave.com/t/arfc-add-contango-protocol-cian-protocol-and-index-coop-to-flashborrowers-on-aave-v3/16478)

<br>

### Payloads

* Base - [proposal payloads](https://basescan.org/address/0xB66ccF5d57BA2F9971930a1076ad02cbBA8AEd8b#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x34D0F918BcD55D9bBbb7040Fd025492D1d479B7f/contract/43114/code#F1#L20)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x6c267Fe8EDa92d1a3feBEF27b5bd179148F696C6#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xD85Ac41B7a6fCD4A1a53d392915EcCC4f3478d4C#code#F1#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0xF618dB47cf3D64e1F6A18438280c9F9112A6C851#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xE0984Ca98BDEf04434cb6E85AD1E1218F3785C52#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal adds flash borrowers on multiple chains to allow them flashloan from the protocol without paying flashloan premiums.
This is an extension of AIP 48 to allow Contango protocol flashloan without paying fees.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe429fac9de84e73ec66c1a2a488ef8988c18c386a452a444258d507a223a9e53](https://etherscan.io/tx/0xe429fac9de84e73ec66c1a2a488ef8988c18c386a452a444258d507a223a9e53)

```
- proposalId: 60
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x2dc3e8cd412fd533a6a66a2042f519341ae0b3cc1ddf2a7f8f8103bde5f922d0
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "11" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "19" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "46" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "8" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "8" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "5" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x2dc3e8cd412fd533a6a66a2042f519341ae0b3cc1ddf2a7f8f8103bde5f922d0" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/60.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/60.md)

**Payload reports**

* Base V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/11.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/11.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/19.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/19.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/46.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/46.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/8.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/8.md)

* BNB - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/8.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/8.md)

* Scroll - No Report

<br>

### Technical analysis

We have verified that on all 6 chains mentioned above the addresses `0xab515542d621574f9b5212d50593cD0C07e641bD` or `0x14F8e5Fe35b2d0D67dBcE9329f1b5d09f60c06C3` were granted flashBorrower roles on AaveV3, according to the specification. 

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

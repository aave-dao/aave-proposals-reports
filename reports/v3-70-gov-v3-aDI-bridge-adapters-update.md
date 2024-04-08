# Proposal 70. Native bridge adapters update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=70](https://vote.onaave.com/proposal/?proposalId=70)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/26](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/26)

<br>

### Payloads

* Ethereum - [proposal payload](https://etherscan.io/address/0x1aAE19C58Bb7ef3aeF70D28BC6E6a7E72a62372b#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x3973A4DaB14f14A103Ec823CEd04F2AFFD518b07#code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xe2561afFb839e6944c47e122BD931EB546712200#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xD66aFdD8DacD2Be9a505eDE2867D014F9F0299eD#code#F1#L1)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x60908614ECdf81cE370c6Bb13fa7D10790e9816b/contract/1088/code#F20#L160)

* Base - [proposal payloads](https://basescan.org/address/0x948A6ee78f50077Dc461b465B94190005C2eE393#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x22191287bC58875f0fd1BB3D28BD985d2dDAc192#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xE0620399C1b964E9DCDf45879295a92B2A3f82df#code#F19#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal adds new bridge adapters on multiple networks to introduce some data visibility and configuration handling changes to the code.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x708b7372dde1fff6c9fa896130bda3995d45f5cfba13029165c11a7d40e38e3d](https://etherscan.io/tx/0x708b7372dde1fff6c9fa896130bda3995d45f5cfba13029165c11a7d40e38e3d)

```
- proposalId: 70
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xe49d4ab826f1db54eda94e9d5ff536cb80d09ea4f0d6d36829f2626c95cac5f1
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "95" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "49" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "23" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "22" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "10" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "15" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "11" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "7" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xe49d4ab826f1db54eda94e9d5ff536cb80d09ea4f0d6d36829f2626c95cac5f1" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/70.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/70.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/95.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/95.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/49.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/49.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/23.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/23.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/22.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/22.md)

* Metis - No Report.

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/15.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/15.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/11.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/11.md)

* Scroll - No Report.

<br>

### Technical analysis

We verified that the payloads are adding the declared bridge adapters on the correct networks as the in the correct role - forwarder/receiver, as stated in the table.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

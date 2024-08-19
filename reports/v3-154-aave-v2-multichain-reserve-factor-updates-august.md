# Proposal 154. Multichain Reserve Factor Updates August.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=154](https://vote.onaave.com/proposal/?proposalId=154)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-bridged-usdc-reserve-factor-across-all-deployments/17787](https://governance.aave.com/t/arfc-increase-bridged-usdc-reserve-factor-across-all-deployments/17787)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xB1c71895C7Ab185AA72cC1DAEAEBF52b3912E56a#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x7EBEDDd200731f16aAf97161B7A374cC3fEC448e#code#F1#L1)
 
* Polygon - [proposal payloads](https://polygonscan.com/address/0x472B5D26153AdA5631f44FAF6108eb263Ff7610b#code#F1#L1) 

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x2C054F2f3852907B96e1bd69d1E39768514a42F4#code#F1#L4) 

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xE4560a1ED5DE3B1BcCfCcD16Bad4F911868e55cB#code#F1#L4) 

* Base - [proposal payloads](https://basescan.org/address/0xAbEBdb559afD8c424495BA059895C20E6C55303C#code#F1#L1) 

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal will reduce deposit yield for assets on Ethereum v2 and Avalanche v2 instances of Aave Protocol by increasing the RF by 5.00%. By increasing the RF a greater portion of the interest paid by borrowers is directed to the Aave DAO's treasury.

This results in a lower deposit rate for users and encourages migration from v2 instances of the Aave Protocol to v3. User's funds are not at risk of liquidation and the borrowing rate remains unchanged.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa3bb7af1cb9e4aef15d09e21b69e08eb1b41d13c2cc1667caa5b24130019b3b0](https://etherscan.io/tx/0xa3bb7af1cb9e4aef15d09e21b69e08eb1b41d13c2cc1667caa5b24130019b3b0)

```
- proposalId: 154
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x48eab28aa5a7cd08dfe029558f73df291c874e854620f8fef9a1be67fde48df4
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
      "payloadId": "163" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "78" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "49" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "45" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "47" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "31" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x48eab28aa5a7cd08dfe029558f73df291c874e854620f8fef9a1be67fde48df4" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/154.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/154.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/163.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/163.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/78.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/78.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/49.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/49.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/45.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/45.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/47.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/47.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/31.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/31.md)


<br>

### Technical analysis

We have verified that the payload setting up the parameters correctly to each asset. We have verified that the liquidity rate change is correct.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

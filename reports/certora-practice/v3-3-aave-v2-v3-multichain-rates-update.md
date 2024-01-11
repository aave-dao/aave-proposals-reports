# Proposal 3. Stablecoin IR Curves Updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/3/](https://app.aave.com/governance/proposal/3/)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-stablecoin-ir-curves-updates/15838](https://governance.aave.com/t/arfc-chaos-labs-stablecoin-ir-curves-updates/15838)

<br>

## Certora analysis

<br>

### Proposal types

Configuration Update

<br>

### Context

This proposal increases stable coins interest rates across all Aave markets and chains to 6% on the slope 1 - the slope representing the interest rate growth below the optimal utility point.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc763476c722b23e8c80260027e384a48117a199406a75692f0a7ccf1ce94e0a1](https://etherscan.io/tx/0xc763476c722b23e8c80260027e384a48117a199406a75692f0a7ccf1ce94e0a1)

```
- id: 414
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c0000000000000000000000000000000000000000000000000000000000000016]
- withDelegatecalls: [false]
- startBlock: 18798764
- endBlock: 18817964
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x92b67c3c943a6674acc652eab792cd3832d095257146e24749d25b9326b04543
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/3.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/3.md)

**Payload reports**

* Ethereum V2 & V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/44.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/44.md)

* Avalanche V2 & V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/12.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/12.md)

* Polygon V2 & V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/25.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/25.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/9.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/9.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/8.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/8.md)

* Base V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/6.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/6.md)

* Metis V3 - []()

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/3.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/3.md)

<br>

### Technical analysis

We have verified that the proposal payloads correctly set the parameters for the stated stable coins across all markets as declared in the IPFS.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. ****

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: All interest rate updates are using the config engine.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

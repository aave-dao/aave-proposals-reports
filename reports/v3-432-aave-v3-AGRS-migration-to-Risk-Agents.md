# Proposal 432. AGRS (Risk Stewards) migration to Risk Agents

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=432)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/122)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xfFc35B2ae62A7a4aCCAa64BCe70eF9c85435b0eC)
* Ethereum - [proposal payloads](https://etherscan.io/address/0x8dA7d151F230ca969a0460Be804Af7aAe5b50f6b)
* Ethereum - [proposal payloads](https://etherscan.io/address/0x90BB7b31bce1C03A646bCD4b26219d3d973690B8)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xeED95cea6E2FD11f1513d2317d4c4353523e76B4)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0x2A31906B9B6da2d9D2057C926276C0D610e798822)

* Optimisim - [proposal payloads](https://optimistic.etherscan.io/address/0x8b5850ADD9784874BCB3cc3ee72B2DE3f897d61A)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x9D1C9aA189c538c0F793ABCCB8A6195A4f67D878)

* Base - [proposal payloads](https://basescan.org/address/0xCC88fB5f07F38e285Aba857ee5345535c60f4098)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x593bBD378c2bdC59A54966135A7653f5e08Ce172)

* BnB - [proposal payloads](https://bscscan.com/address/0x593b820168eeBa2De15eBdAb0F2bCe4c8B09760A)

* Linea - [proposal payloads](https://lineascan.build/address/0xE638b790AF0EFaD986F162A1dDbEa7C0583d3a74)

* Plasma - [proposal payloads](https://plasmascan.to/address/0x2514b2B522dB4FdE44ec8eAe701Be17b204D4c21)




## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades



### Context
#### Simple Summary
Following the approval of Risk Agents, this proposal migrates all existing injector middleware infra used to perform automated risk updates to the new chaos agents system.

#### Motivation
Currently, the AGRS, in conjunction with the injector system, is responsible for processing highly constrained risk recommendations for a range of parameters, including supply and borrow caps, interest rates, pendle pt e-mode collateral params, and CAPO values across multiple assets and Aave instances. These updates are executed through the injector middleware, which consumes updates from the chaos risk oracles and injects updates onto the Aave protocol in real-time.

While the existing system has served Aave more than well, several limitations exist:

Limited generalization: Almost every Risk Stewards activation requires ad-hoc replication of the entire architecture. This results in meaningful overhead for Aave SPs.
Limited infrastructure visibility: Tracking all active Risk Stewards, as well as their covered assets and constraints, can be challenging at times.
The Chaos Risk Agents framework generalizes and modularizes the process of ingesting Risk Oracle data within Aave. It eliminates redundant deployments, centralizes validation logic, and improves visibility across all risk automation layers. The result is a cleaner, more maintainable architecture that allows Aave to expand real-time risk management capabilities, ensuring consistent, verifiable execution of parameter updates.

### Proposal Creation
Transaction: [0x7a80c84621cecdf7f6e626fc9f861d5adedfd680fb36ea157ea87ecc88a5f97e](https://etherscan.io/tx/0x7a80c84621cecdf7f6e626fc9f861d5adedfd680fb36ea157ea87ecc88a5f97e)
- `proposalId`: 432
- `creator`: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- `accessLevel`: 1
- `ipfsHash`: 0xc8bf42a0cfd263e9ab0c78ab8a94141e26a40ad19b77636a2c9c163d1e05245e

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "390" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "136" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "104" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "91" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "108" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "92" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "69" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "53" 
    }, 
    { 
      "chain": "59144", 
      "accessLevel": "1", 
      "payloadsController": "0x3BcE23a1363728091bc57A58a226CF2940C2e074", 
      "payloadId": "19" 
    }, 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "14" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0xc8bf42a0cfd263e9ab0c78ab8a94141e26a40ad19b77636a2c9c163d1e05245e" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/390.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/390.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/136.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/104.md)

* Optimisim - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/91.md)

* Arbitrum - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/108.md)

* Base - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/92.md)

* Gnosis - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/69.md)

* BnB - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/53.md)

* Linea - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/19.md)

* Plasma - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/14.md)


### Technical Analysis

- We have validated the full Chaos Risk Agents migration across all supported networks, confirming correct deployment of AgentHub and automation contracts, proper governance executor ownership and proxy-admin configuration, and correct linkage between AgentHub and agent-hub-automation.

- Update type consistency was verified end-to-end across RiskOracle, injector contracts, AgentHub registrations, and agent payload definitions, accounting for known update-type renames and scoped differences per network.
 
- Access control was reviewed to ensure all legacy injector RISK_ADMIN roles were revoked and privileges are exclusively granted to the new agent contracts.
  
- Chainlink automations were validated, including cancellation of legacy automations, correct registration of new upkeeps, and verification of upkeepCheckData.
  
- Encoding and decoding compatibility between RiskOracle-emitted data and agent contract logic was confirmed by comparing legacy injector decoding with new agent implementations.
  
- Completeness was ensured by validating that all agents and risk parameters previously activated via historical AIPs are included in the current registration.
 
- Finally, configuration parity was confirmed by verifying that market coverage and risk range configurations on the new agents exactly match those of the existing edge-args injector system.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
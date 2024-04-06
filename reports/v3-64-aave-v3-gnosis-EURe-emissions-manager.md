# Proposal 64. EURe Emissions Manager.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=64](https://vote.onaave.com/proposal/?proposalId=64)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-set-aci-as-emissions-manager-for-eure-on-aave-v3-gnosis-market/17130](https://governance.aave.com/t/arfc-set-aci-as-emissions-manager-for-eure-on-aave-v3-gnosis-market/17130)

<br>

### Payloads

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x17C5BfaB1155704b20F3ff8DD408B7cBc02811F6#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal propose to set an emission manager for EURe on gnosis chain to incentivize growth of Aave on the gnosis chain.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5c6ee5059835e0fc2618486ee22387f6f76ce090870c3e623e2c6e8ae60b66b3](https://etherscan.io/tx/0x5c6ee5059835e0fc2618486ee22387f6f76ce090870c3e623e2c6e8ae60b66b3)

```
- proposalId: 64
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x06d204eae05f9299d21226c4e4a29f90e3c6cda4c22d3175cca85ce2e1c30f35
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "9" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x06d204eae05f9299d21226c4e4a29f90e3c6cda4c22d3175cca85ce2e1c30f35" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/64.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/64.md)

**Payload reports**

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/9.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/9.md)

<br>

### Technical analysis

We have verified that the payload is setting declared ACI multisig as the emission admin of EURe over the gnosis chain and has no further side effects.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

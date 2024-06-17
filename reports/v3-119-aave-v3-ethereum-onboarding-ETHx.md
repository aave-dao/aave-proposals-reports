# Proposal 113. Onboard USDe Aave V3 Ethereum.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=119](https://vote.onaave.com/proposal/?proposalId=119)

<br>

### Governance forum discussion

[https://ghttps://governance.aave.com/t/arfc-onboarding-ethx-to-aave-v3-ethereum/15672](https://governance.aave.com/t/arfc-onboarding-ethx-to-aave-v3-ethereum/15672)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x94cdd72ee5Ba46b9132E99957085Fc4467c50350#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboards ETHx onto Ethereum V3 in order to improve the diversity of assets on Aave and bolster liquidity within the ecosystem.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x917cc29fb5ad9abd7232000f80f8008471badac75d8126454c2087f01a39eec3](https://etherscan.io/tx/0x917cc29fb5ad9abd7232000f80f8008471badac75d8126454c2087f01a39eec3)

```
- proposalId: 119
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x97c348f2ab5a533a551aeb5021bd4c3953fb85e37dbf2e8a5240c61052c04e39
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
      "payloadId": "136" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x97c348f2ab5a533a551aeb5021bd4c3953fb85e37dbf2e8a5240c61052c04e39" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/119.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/119.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/136.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/136.md)

<br>

### Technical analysis

We have verified that the payload onboards ETHx to Ethereum V3 with the same configuration declared in the IPFS.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

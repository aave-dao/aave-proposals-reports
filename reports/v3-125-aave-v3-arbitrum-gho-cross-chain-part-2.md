# Proposal 125. GHO Cross-Chain - Part 2.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=125](https://vote.onaave.com/proposal/?proposalId=125)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-cross-chain-launch/17616](https://governance.aave.com/t/arfc-gho-cross-chain-launch/17616)

<br>

### Payloads

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x81b69029b733491fFD5A274d4Ef33F443245253e#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal is the second part of the GHO-Cross-Chain plan the first can be found here:[AIP-120](https://vote.onaave.com/proposal/?proposalId=120).

This part onboards GHO onto Arbitrum V3 in order to improve the diversity of assets on Aave and bolster liquidity within the ecosystem.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x617f271f41ba845b35b84d66ed614c8f3ff4d806ec9107749861d9bfa11fc601](https://etherscan.io/tx/0x617f271f41ba845b35b84d66ed614c8f3ff4d806ec9107749861d9bfa11fc601)

```
- proposalId: 125
- creator: 0x66a28531e6f390a8cd44ab0c57a0f1aeb7e673ff
- accessLevel: 1
- ipfsHash: 0xc343a4460b002ad0612a04bc9d0a8081027652331200136e40740dba5f6ba106
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "35" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xc343a4460b002ad0612a04bc9d0a8081027652331200136e40740dba5f6ba106" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/125.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/125.md)

**Payload reports**

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/35.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/35.md)

Note that the seatbelt may revert due to the executor not having any GHO balance, but we were assured that by the time of execution the executor will have enough GHO in it's balance.

<br>

### Technical analysis

We have verified that the payload onboards GHO to Arbitrum V3 with the same configuration declared in the IPFS.

<br>

The proposal is consistent with the description on the governance forum apart from the variableSlope1 which was adjusted from 12% to 13%.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

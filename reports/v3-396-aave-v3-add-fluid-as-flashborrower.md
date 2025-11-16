# Proposal 396. Add Fluid Protocol to flashBorrowers on Plasma


### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=396)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-add-fluid-protocol-to-flashborrowers-on-plasma/23252)

### Payloads

* Plasma - [proposal payloads](https://plasmascan.to/address/0xf31DF259cCD67f5C84b212379C1FC59170Fd564a)


## Certora Analysis

### Proposal Types


* :handshake: Permission granting and revoking


### Context
This proposal includes Fluid Protocol on the Aave v3 Flashborrowers whitelist for Plasma.
Fluid has been a long-standing partner in the Aave ecosystem, providing valuable infrastructure and user interfaces. This publication extends the flashloan fee waiver to include recent Fluid deployment on Plasma.


### Proposal Creation
Transaction: [0x79d1b4a6c22e63a9e48e4cef1e46617b853ccd8395f26b2c077e0e5f3356e255](https://etherscan.io/tx/0x79d1b4a6c22e63a9e48e4cef1e46617b853ccd8395f26b2c077e0e5f3356e255)
- `proposalId`: 396
- `creator`: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x9f40df3cd3322153ae2cf035a480953fda9e5df2cfc1bb04f9f668983cf8e1d7

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "6" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0x9f40df3cd3322153ae2cf035a480953fda9e5df2cfc1bb04f9f668983cf8e1d7" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/6.md)

**Payload Reports**

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/6.md)



### Technical Analysis
We verified that the whitelisted contract address is consistent across the forum post, IPFS metadata, and the on-chain payload. We executed and reviewed the payload to confirm it performs only the intended addFlashBorrower() call and targets the correct address. All checks passed and the Seatbelt report shows no irregularities.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
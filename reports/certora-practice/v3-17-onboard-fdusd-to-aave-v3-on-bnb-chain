# Proposal 17. Onboard fdUSD to Aave v3 on BNB chain.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=17](https://vote.onaave.com/proposal/?proposalId=17)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-fdusd-to-aave-v3-on-bsc/16364](https://governance.aave.com/t/arfc-onboard-fdusd-to-aave-v3-on-bsc/16364)

<br>

### Payloads

* BNB - [proposal payloads](https://bscscan.com/address/0xe86F628f0711bf9ccE64881713290F68eC046621#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: listing new assets

<br>

### Context

This proposal aims to onboard the fdUSD stable coin on the Aave-v3 protocol on BNB network.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x20f65433c968fbbdc70c3e902b58793bef31298b16cbbc4a2a3ba70dc2dc2a0d](https://etherscan.io/tx/0x20f65433c968fbbdc70c3e902b58793bef31298b16cbbc4a2a3ba70dc2dc2a0d)

```
- proposalId: 17
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xbacf3a4c8a68f5859cf7cd78c46e303f54d735fdf27c798b70e7597e7d246f13
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "56",
      "accessLevel": 1,
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
      "payloadId": "2"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xbacf3a4c8a68f5859cf7cd78c46e303f54d735fdf27c798b70e7597e7d246f13"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/17.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/17.md)

**Payload reports**

* BNB V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/2.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/2.md)

<br>

### Technical analysis

We have verified that the payload executing the following actions:

- listing the fdUSD stable coin with the parameters according to the specified table in the IPFS. 

- supplying 1 fdUSD to the BNB collector to prevent first depositor attack.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

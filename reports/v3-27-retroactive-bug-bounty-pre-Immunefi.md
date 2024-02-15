# Proposal 14. Retroactive Bug Bounty Pre-Immunefi.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=27](https://vote.onaave.com/proposal/?proposalId=27)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-retroactive-bug-bounties-proposal-pre-immunefi/15989](https://governance.aave.com/t/bgd-retroactive-bug-bounties-proposal-pre-immunefi/15989)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xc7950e9591A6e3d7fb68b0d289dD4e54167f1B70#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is a bounty payment execution for security reports submitted by white hats before Aave's bug bounty program on immunify was activated.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc40f2ebe1e25e5d36d1de202a2cc1d3a3672c5409e2885d9af59aab0bb2141c3](https://etherscan.io/tx/0xc40f2ebe1e25e5d36d1de202a2cc1d3a3672c5409e2885d9af59aab0bb2141c3)

```
- proposalId: 27
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xd0152546a8ca4884b82b7f7c9f97a2ae601361efebb52cfd3ff71d345c2c7c68
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
      "payloadId": "62"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xd0152546a8ca4884b82b7f7c9f97a2ae601361efebb52cfd3ff71d345c2c7c68"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/27.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/27.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/62.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/62.md)

<br>

### Technical analysis

We have verified that the payload executes the following actions:

- transfer 65,000 aUSDC to the address 0xFa760444A229e78A50Ca9b3779f4ce4CcE10E170. 

- transfer 15,000 aUSDC to the address 0x7dF98A6e1895fd247aD4e75B8EDa59889fa7310b.

- transfer 6,500 aUSDC to the immunify which is the fee corresponding to the 10% of the bounty being paid.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

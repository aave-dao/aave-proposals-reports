# Proposal 138. Risk Parameter Updates - sAVAX on Aave V3 Avalanche.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=138](https://vote.onaave.com/proposal/?proposalId=138)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-savax-on-aave-v3-avalanche-07-16-2024/18277](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-savax-on-aave-v3-avalanche-07-16-2024/18277)

<br>

### Payloads

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x564Dfd09eBB63F7e468401AffE2d8c2cDD08D68D/contract/43114/code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal modifies the LTV and LT of sAVAX on Avalanche-V3 market in order to allow Aave to enhance user's capital efficiency.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x665bc588059879befdd9822250325f94528b675bfe7cdae65b1bc5dcef7f15a8](https://etherscan.io/tx/0x665bc588059879befdd9822250325f94528b675bfe7cdae65b1bc5dcef7f15a8)

```
- proposalId: 138
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0xa8c3145a62879685b5569daf860b7d65dd1c9affc796c90c26498f95646b9a98
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "43114",
      "accessLevel": "1",
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
      "payloadId": "43"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xa8c3145a62879685b5569daf860b7d65dd1c9affc796c90c26498f95646b9a98"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/138.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/138.md)

**Payload reports**

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/43.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/43.md)

<br>

### Technical analysis

We have verified that the payload modifies following parameters of sAVAX on Avalanche-V3:

- LTV: 30% -> 40%

- LT: 40% -> 45%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


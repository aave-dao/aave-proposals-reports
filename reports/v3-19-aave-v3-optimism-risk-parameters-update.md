# V3. Proposal 19. Aave v3 Optimism - MAI risk parameters update

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=19](https://vote.onaave.com/proposal/?proposalId=19)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gauntlet-recommendation-for-mai-mimatic-deprecation-phase-2/15957](https://governance.aave.com/t/arfc-gauntlet-recommendation-for-mai-mimatic-deprecation-phase-2/15957)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates risk parameters on Aave v3 Optimism for MAI.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9e139b76905fd26f6e3218f3070e1c3161c980b6e8a57b26e840218a1ddffc85](https://etherscan.io/tx/0x9e139b76905fd26f6e3218f3070e1c3161c980b6e8a57b26e840218a1ddffc85)


```
- proposalId: 19
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- accessLevel: 1
- ipfsHash: 0xf6328acd631e4aac9d1e14e98d4bc56f0a852f496afb7c5e3d5254e2757ce353
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "10",
      "accessLevel": 1,
      "payloadsController": "0x0e1a3af1f9cc76a62ed31ededca291e63632e7c4",
      "payloadId": "12"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0xf6328acd631e4aac9d1e14e98d4bc56f0a852f496afb7c5e3d5254e2757ce353"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/19.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/19.md)

**Payloads report**

**Optimism**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/12.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/12.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/12_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/12_forge.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://optimistic.etherscan.io/address/0x2a1cb7834E36b318c5ad1939C45Ce3e365b92A7d#code#F1#L15) does the following changes on Aave v3 Optimism:

**MAI**

- LT: 65% -> **1%**

<br>

The proposal payload is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

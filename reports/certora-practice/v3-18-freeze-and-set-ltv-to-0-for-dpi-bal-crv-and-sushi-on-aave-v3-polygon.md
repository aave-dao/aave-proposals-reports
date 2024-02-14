# Proposal 18. Freeze and set LTV to 0 for DPI, BAL, CRV, and SUSHI on Aave v3 Polygon, 2024.01.19

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=18](https://vote.onaave.com/proposal/?proposalId=18)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-recommendation-to-freeze-and-set-ltv-to-0-on-low-cap-aave-v3-polygon-collateral-assets/16311](https://governance.aave.com/t/arfc-recommendation-to-freeze-and-set-ltv-to-0-on-low-cap-aave-v3-polygon-collateral-assets/16311)

<br>

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0x0090986Ad3772306B90958316370363b2D1a896A#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal sets the LTV to 0 and freezes the following tokens on Aave-v3-Polygon: DPI, BAL, CRV, and SUSHI.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1594a4417e3251d27e90841b1c82637e91eae49f733ad50a1138156ad21a6735](https://etherscan.io/tx/0x1594a4417e3251d27e90841b1c82637e91eae49f733ad50a1138156ad21a6735)

```
- proposalId: 18
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- accessLevel: 1
- ipfsHash: 0xaa892464bae2973847f53df2175ab6c1c3240656eef5d72fa76210f50bb56d1d
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "137",
      "accessLevel": 1,
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
      "payloadId": "33"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xaa892464bae2973847f53df2175ab6c1c3240656eef5d72fa76210f50bb56d1d"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/18.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/18.md)

**Payload reports**

* Polygon V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/33.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/33.md)

<br>

### Technical analysis

We have verified that the payload modifies the LTV of DPI, BAL, CRV, and SUSHI across the polygon network to 0 and freezes those tokens.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

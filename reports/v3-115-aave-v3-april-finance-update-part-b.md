# Proposal 115. April Finance Update Part B.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=115](https://vote.onaave.com/proposal/?proposalId=115)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-april-finance-update/17390](https://governance.aave.com/t/arfc-april-finance-update/17390)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xeA29C0424769b5107AC94C7F9c635464a319701D#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is part B of [AIP 103](https://app.aave.com/governance/v3/proposal/?proposalId=103) which is a collection of treasury management actions that mainly aim to consolidate the ecosystem holdings in gho and preparing treasury for upcoming expected expenses.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1b7e048bd5fd859b929427a5a0503552ecd12de65362216dcc3f451b12f306e0](https://etherscan.io/tx/0x1b7e048bd5fd859b929427a5a0503552ecd12de65362216dcc3f451b12f306e0)

```
- proposalId: 115
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xe3183b06212ae8d1c10b61a2f22d6aba7f4490ae909caafbe81d3d0daaff2086
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
      "payloadId": "134" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xe3183b06212ae8d1c10b61a2f22d6aba7f4490ae909caafbe81d3d0daaff2086" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/115.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/115.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/134.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/134.md)

<br>

### Technical analysis

We have verified that the payload is executing the following actions:

- Swap all DAI that was bridged from Polygon during part A (around 500,000 uints)

- Create an allowance for ALC safe of 1,000,000$ in USDC and 1,000,000$ in aEthUSDT

- Deposit into V3 the collector balance of WETH, WBTC and USDC-1,000,000 (the 1,000,000 we approved to the ALC safe)

<br>

The proposal is consistent with the description on the governance forum

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

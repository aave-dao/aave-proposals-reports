# Proposal 86. V2 Stable Debt Offboarding.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=86](https://vote.onaave.com/proposal/?proposalId=86)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-full-deprecation-of-stable-rate/16473](https://governance.aave.com/t/bgd-full-deprecation-of-stable-rate/16473)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x64c604E483A6E04692B5c87Db9561529feBffC17#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade

<br>

### Context

This proposal upgrades the v2 pool implementation and introduces a new method swapToVariable which allows permission-less swapping from stable to variable debt, as part of stable rate deprecation.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5cf938378ba3c7449504578d32e62a0612bfc237b152ed560da223f587b6410c](https://etherscan.io/tx/0x5cf938378ba3c7449504578d32e62a0612bfc237b152ed560da223f587b6410c)

```
- proposalId: 86
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xe8e62cf3cb3fc0fc5686ce63c64f16e14d4bfb58053d74189540f66a607bbea5
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
      "payloadId": "111" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xe8e62cf3cb3fc0fc5686ce63c64f16e14d4bfb58053d74189540f66a607bbea5" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/86.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/86.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/111.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/111.md)

<br>

### Technical analysis

We have verified that the payload upgrades the v2 pool implementation with the following:

- Introduce a new method swapToVariable(address asset, address user) that allows permission-less swapping from stable to variable debt.

- Change the method swapBorrowRateMode(address asset, uint256 rateMode) to only allow swap between stable to variable.

- Change the validationLogic function validateSwapRateMode will now check that the current rate is stable.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

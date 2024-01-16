# V3. Proposal 5. Treasury management - Stablecoins consolidation

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=5](https://vote.onaave.com/proposal/?proposalId=5)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-funding-update/15194/13](https://governance.aave.com/t/arfc-aave-funding-update/15194/13)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal consolidates different stablecoin holdings on the treasury doing multiple operations: migrating from v2 to v3, deposit funds currently held in underlying to Aave v2 and swapping some USDC and DAI to GHO.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x75bf1487de680b43a7bc4a7dbceedff6d7a70cdd8eec266cd6f6a9ff44165ac7](https://etherscan.io/tx/0x75bf1487de680b43a7bc4a7dbceedff6d7a70cdd8eec266cd6f6a9ff44165ac7)


```
- proposalId: 5
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x57dec17b5950c76b33917a2ff61784a85c796c9fc061e91d313b3fc8a23e6ecf
```

**createProposal() parameters**
```
[
  {
    "chain": "1",
    "accessLevel": 1,
    "payloadsController": "0xdabad81af85554e9ae636395611c58f7ec1aaec5",
    "payloadId": "46"
  }
]
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/5.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/5.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/46.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/46.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x1F5cD22582B4cD85fF8382Fd40B88776470C38fc#code#F1#L19) does the following:

1. Redeems from Aave v2 Ethereum almost the whole balance of USDC, currently amounting to ~1'786'000 USDC.
2. Deposits ~2'480'000 USDC into Aave v3 Ethereum. From the funds redeemed before from v2 and 1'700'000 held before in USDC by the Collector.
3. Deposit 750'000 USDT into Aave v3 Ethereum.
4. Swaps 1'000'000 USDC to GHO, by using the AaveSwapper (CowSwap + Milkman).
5. Swaps 500'000 DAI to GHO, by using the AaveSwapper (CowSwap + Milkman).

<br>

The proposal payload is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

# V3. Proposal 17. Aave v3 BNB - fdUSD listing

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=17](https://vote.onaave.com/proposal/?proposalId=17)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-fdusd-to-aave-v3-on-bsc/16364](https://governance.aave.com/t/arfc-onboard-fdusd-to-aave-v3-on-bsc/16364)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

:wrench: :bar_chart: params-update

<br>

### Context

This proposal lists native fdUSD (First Digital USD) on the Aave v3 BNB Chain pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x20f65433c968fbbdc70c3e902b58793bef31298b16cbbc4a2a3ba70dc2dc2a0d](https://etherscan.io/tx/0x20f65433c968fbbdc70c3e902b58793bef31298b16cbbc4a2a3ba70dc2dc2a0d)


```
- proposalId: 17
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xbacf3a4c8a68f5859cf7cd78c46e303f54d735fdf27c798b70e7597e7d246f13
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "56",
      "accessLevel": 1,
      "payloadsController": "0xe5ef2dd06755a97e975f7e282f828224f2c3e627",
      "payloadId": "2"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0xbacf3a4c8a68f5859cf7cd78c46e303f54d735fdf27c798b70e7597e7d246f13"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/17.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/17.md)

**Payloads report**

**BNB Chain**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/2.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/2.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://bscscan.com/address/0xe86F628f0711bf9ccE64881713290F68eC046621#code#F1#L18) lists fdUSD with the following configuration:

- The asset is enabled for borrowing and the interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 6%
  - Variable borrow slope 2: 75%
  - Optimal point: 90%

- The asset is enabled as collateral
- LTV: 70%
- Liquidation Threshold: 75%
- Liquidation Bonus: 5%
- Liquidation Protocol fee: 10%
- Reserve Factor: 20%
- Supply cap: 8'000'000 fdUSD
- Borrow cap: 7'500'000 fdUSD
- No eMode category
- Flashlonable
- Enabled for borrowing in isolation

The oracle used is a [Chainlink fdUSD/USD](https://bscscan.com/address/0x390180e80058A8499930F0c13963AD3E0d86Bfc9#readContract#F8).

<br>

The proposal payload is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

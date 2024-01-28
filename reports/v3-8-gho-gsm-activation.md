# V3. Proposal 8. GHO - GSM (GHO Stability Module) activation

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=8](https://vote.onaave.com/proposal/?proposalId=8)

<br>

### Governance forum discussion

[https://governance.aave.com/t/gho-stability-module-update/14442](https://governance.aave.com/t/gho-stability-module-update/14442)

<br>

## BGD analysis

<br>

### Proposal types

gho

<br>

### Context

This proposal activates the GHO Stability Module (GSM) smart contracts, allowing for 1:1 swapping GHO<>USDC and GHO<>USDT in its 2 instances.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x911fc8cf98304a3c93c67742f6e86350994eeb83e7ddb5b57285619ba92e62cf](https://etherscan.io/tx/0x911fc8cf98304a3c93c67742f6e86350994eeb83e7ddb5b57285619ba92e62cf)


```
- proposalId: 8
- creator: 0x99c7a4a4ab99882c422ef777b182ebda204d5b02
- accessLevel: 1
- ipfsHash: 0xb87ef765d6082f5ac26466bc730b069c42d4ea9fe130250a26be627ac259d259
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdabad81af85554e9ae636395611c58f7ec1aaec5",
      "payloadId": "48"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0xb87ef765d6082f5ac26466bc730b069c42d4ea9fe130250a26be627ac259d259"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/8.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/8.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/48.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/48.md)

<br>

### Technical analysis

A deep review of the GSM smart contract is out of the scope of this report, as it was already done by security entities engaged with the DAO. However, we have verified the proposal is consistent with what it intends, and its [payload](https://etherscan.io/address/0x81e6AB07Dbf496CE609aC672c08cBD66bA2817eA#code#F1#L79) does the following:
1. Enables both GHO<>USDC and GHO<>USDT GSM instances as GHO facilitators, with 500'000 GHO capacity each.
2. Grants `SWAP_FREEZER_ROLE` on each GSM instance to the Oracle Swap Freezer smart contract, automating halting swaps under specific conditions. This is enabled via the Aave Robot system, including funding it with 80 LINK.
3. Enables the new fixed fee strategy on each GSM; contract in charge of implementing the logic to calculate swap fees (0.2% on buy and sell directions).

In addition, we have verified that only the entities intended have permissions on the GSM system.

<br>

The proposal is consistent with its description, and generally with Snapshot. Only the underlying price range has changed (setting one), which seems totally reasonable.



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

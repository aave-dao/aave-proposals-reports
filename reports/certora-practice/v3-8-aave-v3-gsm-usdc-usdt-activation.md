# Proposal 3. Stablecoin IR Curves Updates

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=8](https://vote.onaave.com/proposal/?proposalId=8)

<br>

### Governance forum discussion

[https://governance.aave.com/t/gho-stability-module-update/14442](https://governance.aave.com/t/gho-stability-module-update/14442)

<br>

## Certora analysis

<br>

### Proposal types

:ghost: gho facilitator activation

<br>

### Context

The proposal activates two new facilitators gsm-usdc and gsm-usdt. 


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x911fc8cf98304a3c93c67742f6e86350994eeb83e7ddb5b57285619ba92e62cf](https://etherscan.io/tx/0x911fc8cf98304a3c93c67742f6e86350994eeb83e7ddb5b57285619ba92e62cf)

```
- proposalId: 8
- creator: 0x99c7a4a4ab99882c422ef777b182ebda204d5b02
- accessLevel: 1
- ipfsHash: 0xb87ef765d6082f5ac26466bc730b069c42d4ea9fe130250a26be627ac259d259
```

<br>

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdabad81af85554e9ae636395611c58f7ec1aaec5",
      "payloadId": "48"
    },
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0xb87ef765d6082f5ac26466bc730b069c42d4ea9fe130250a26be627ac259d259"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/8.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/8.md)

**Payload reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/48.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/48.md)

<br>

### Technical analysis

We have verified that the proposal payload correctly:
1. Adds the two stability modules as facilitators of gho tokens with 500,000 gho cap and exposure cap of 500,000 underlying assets.
2. Sets the Lv1 executor as well as a dedicated swap freezer contract as swap freezers of the stability modules. The swap freezers are set with the lower and upper boundaries as declared.
3. Sets the fee strategy for both of the stability modules, with both a buy and sell fee of 0.2%.
4. Adds both stability modules to the gsm registry.
5. Sets the `AaveCLRobotOperator` as a keeper of the swap freezer, loading it with 80 LINK for each of the stability modules.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: All relevant registries were updated to include the new modules.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

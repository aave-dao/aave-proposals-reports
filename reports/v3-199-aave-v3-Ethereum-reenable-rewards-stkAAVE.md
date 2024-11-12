# Proposal 199. Safety Module stkAAVE - Re-enable Rewards


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=199](https://vote.onaave.com/proposal/?proposalId=199)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-amend-safety-module-emissions/16640/13](https://governance.aave.com/t/arfc-amend-safety-module-emissions/16640/13)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x477307bC08a7BBDbAD2C932B4B77eE96dd2d5B5b#code)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal aims to renewing the AAVE emissions to stkAAVE holders for the following 180 days.
With the conclusion of the recent reward cycle, this proposal aims to renew $AAVE emissions for stkAAVE holders. The stkAAVE module has proven to be a crucial mechanism as an AAVE supply sink, currently holding a TVL of $480M and accounting for 18.8% of the supply.
It is recommended to maintain these emissions in anticipation of upcoming Umbrella developments, with adjustments to be made following the outcomes of the Umbrella upgrade.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xba04900fca46c65797d22df17141e885a666225253829b99c8138623d909dde6](https://etherscan.io/tx/0xba04900fca46c65797d22df17141e885a666225253829b99c8138623d909dde6)

```
- proposalId: 199
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x315b3aa83bf146c7733f371552c641726508fc9cb061a159ecacadc0d4eacaa7
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
      "payloadId": "205" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x315b3aa83bf146c7733f371552c641726508fc9cb061a159ecacadc0d4eacaa7" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/199.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/199.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/205.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/205.md)

<br>

### Technical analysis

We have verified that the [proposal payload](https://etherscan.io/address/0x477307bC08a7BBDbAD2C932B4B77eE96dd2d5B5b) does the following:

1. **Configure emission of AAVE tokens on [stkAAVE](https://etherscan.io/address/0x4da27a545c0c5B758a6BA100e3a049001de870f5) with the following parameters:**
   - **Emission**: 360 AAVE per day, set as emission per second (4.1666...e18 wei per second).
   - **Distribution Duration**: 180 days from proposal execution.

2. **Approve AAVE tokens from the Aave Ecosystem Reserve to stkAAVE, allowing stakers to claim them:**
   - The contract first resets the current approval of AAVE tokens to zero.
   - It then sets a new approval amount based on the remaining allowance plus the required distribution amount for the 180-day period.
   - **Total Approval Amount**: Existing remaining allowance + 64,800 AAVE.

#### Explanation of the Approval Reset Mechanism

To adhere to ERC20 standards and avoid potential race conditions, the contract first sets the current approval to zero before setting a new approval amount. This best practice ensures that any unspent tokens from prior allowances are included in the updated approval, maximizing fund efficiency and preventing token lockup.

#### Summary

This proposal extends AAVE rewards for `stkAAVE` stakers at a rate of 360 AAVE/day for an additional 180 days, ensuring efficient and secure reward distribution from the Ecosystem Reserve.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


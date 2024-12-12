# Proposal 214. Onboard GHO and Migrate Streams to Prime Instance


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=214](https://vote.onaave.com/proposal/?proposalId=214)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-gho-and-migrate-streams-to-lido-instance/19686](https://governance.aave.com/t/arfc-onboard-gho-and-migrate-streams-to-lido-instance/19686)

<br>

### Payloads

* Ethereum Lido - [proposal payloads](https://etherscan.io/address/0xF733CD0D599c8316792Ff3740b3A2ceB286FA8De#code)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal seeks to onboard GHO as a borrow-only asset to the Prime instance of Aave v3, with a 3M GHO seed from the Collector and an additional 3M GHO acquired from the spot market. It aims to generate yield for the Aave DAO, enhance GHO’s utility, and ensure sufficient liquidity for Merit allowance. Additionally, it proposes migrating Merit allowances to the Prime market and canceling the Aave Grants DAO GHO allowance.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0de117e8dbb7386c4ae8b27ae296e6c621afc7a237ea8f564c64261874a98678](https://etherscan.io/tx/0x0de117e8dbb7386c4ae8b27ae296e6c621afc7a237ea8f564c64261874a98678)

```
- proposalId: 214
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xd642b2c392ecefe426be16546afc7be5028ff77ca75b2c9362f79a79ab4de487
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
      "payloadId": "218" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xd642b2c392ecefe426be16546afc7be5028ff77ca75b2c9362f79a79ab4de487" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/214.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/214.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/218.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/218.md)


<br>

### Technical analysis

In our review of the proposal, we conducted the following checks:

1. Verified the **AGD allowance** is set to zero.
2. Confirmed the **migration of the Merit allowance** to the Prime instance.
3. Validated the **swap amounts** for:
   - aUSDT: 1.5M
   - aEthUSDT: 0.5M
   - aEthUSDC: 1.0M
4. Cross-checked the **addresses** of the price checker, oracles, and Milkman contract.
5. Ensured the **parameter configurations** for GHO are correct, including:
   - Supply caps
   - Borrow caps
   - Reserve factor
   - Interest rate strategy
6. Verified that GHO is properly added to the **eMode categories** (sUSDe and ezETH).
7. Noted a typo in the IPFS documentation where the **Liquidation Threshold for ezETH eMode** was incorrectly stated as 80% instead of the configured 78%.

All elements align with the proposal’s objectives, except for the documentation typo, which has been flagged..

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


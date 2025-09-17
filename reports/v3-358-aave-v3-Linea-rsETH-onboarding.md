# Proposal 358. Onboard rsETH to Aave V3 Linea Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=358)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-rseth-to-aave-v3-linea-instance/22172)

### Payloads

* Linea - [proposal payloads](https://lineascan.build/address/0x37D3c1eddBCaA4b2e74156D2C6aD3224027EE7A4)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This proposal seeks to onboard rsETH to the Aave V3 deployment on the Linea network.

As the onboarding of rsETH has already been approved and executed on the Ethereum, Arbitrum, and Base Aave V3 instances, this proposal follows the Direct-to-AIP path to extend rsETH support to the Linea instance without repeating the full ARFC process.

### Proposal Creation
Transaction: [0xa7d7db313f4376ee2657a3bf37d79a089a90ccf6ac11f3596c16c77346cb7513](https://etherscan.io/tx/0xa7d7db313f4376ee2657a3bf37d79a089a90ccf6ac11f3596c16c77346cb7513)
- `proposalId`: 358
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xe2d5e82594c356931465f14b6d7110e1a0b38a0536090f21312b73243139bd49

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 12,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xe2d5e82594c356931465f14b6d7110e1a0b38a0536090f21312b73243139bd49",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/358.md)

**Payload Reports**

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/12.md)


### Technical Analysis
We have verified the risk parameters that were configured matches the ipfs and forum, including the emode.
We have validated the token address and price oracles.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
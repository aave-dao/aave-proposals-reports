# Proposal 296. Aave Liquidity Committee Funding Phase VI

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=296)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-liquidity-committee-funding-phase-vi/21682)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x183F144A87586dfe089D9bae5F24A799fdB7a604)



## Certora Analysis

### Proposal Types
* :moneybag: :receipt: Asset transfers

* :handshake: Permission granting and revoking


### Context
This publication presents the Aave Liquidity Committee (ALC) Phase VI Funding request. The payload itself create allowance for the ALC to withdraw 3,500,000 aEthLidoGHO from the Ethereum collector. ALC Ethereum SAFE: 0xA1c93D2687f7014Aaf588c764E3Ce80aF016229b

### Proposal Creation
Transaction: [0x2efc500621ed1b99ed4790bfd329654d1f1c302ce76afd90bb9a471121613f27](https://etherscan.io/tx/0x2efc500621ed1b99ed4790bfd329654d1f1c302ce76afd90bb9a471121613f27)
- `proposalId`: 296
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x22262761d78b56bc43694c7a928aec29b984dd41f4e3ee3ed767e4af4b248e5c

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 273,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x22262761d78b56bc43694c7a928aec29b984dd41f4e3ee3ed767e4af4b248e5c",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/296.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/273.md)


### Technical Analysis
We have verified the amount specified in the allowance is equal to the amount in the payload.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
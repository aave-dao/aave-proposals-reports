# Proposal 217. Onboard SCR to Aave V3 Scroll

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=217)

### Governance Forum Discussions
[Link to forum discussions](https://governance.aave.com/t/arfc-onboard-scr-to-aave-v3-scroll-instance/19688)

### Payloads

* Scroll - [proposal payloads](https://scrollscan.com/address/0xA70404a50Fde6e55Db2b1C5F65aEd8906646Fa11)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking

* :gem: :new: Listing new assets

### Context
The proposal aims to onboard SCR, the native token of Scroll, to Aave V3 on the Scroll Layer 2 blockchain, expanding DeFi opportunities for users by enabling them to borrow SCR.

### Proposal Creation
Transaction: [0x2e3b88f827bcd61654e8771c1e9228216ffb863967a04a4da96a3442b1c15008](https://etherscan.io/tx/0x2e3b88f827bcd61654e8771c1e9228216ffb863967a04a4da96a3442b1c15008)
- `proposalId`: 217
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xf5846ed4aa5069fb719188eb682e8479788091da370edefc18695d1961d63878

**`createProposal()` Parameters**
```
{
    "payloads": [
        {
            "chain": "534352",
            "accessLevel": 1,
            "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            "payloadId": 29
        }
    ],
    "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    "ipfsHash": "0xf5846ed4aa5069fb719188eb682e8479788091da370edefc18695d1961d63878"
}
```

### Aave Seatbelt Report
**Proposal Report**
[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/217.md)

**Payload Reports**

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/29.md)


### Technical Analysis
We compared the parameters in the proposal, verifying alignment between the IPFS and the Solidity payload. The first deposit protection was confirmed through the 100 SCR seed deposit mechanism. The price feed for SCR was validated at the specified oracle address. The parameters were accurately implemented. Lastly, the emission admin was properly assigned to both SCR and its corresponding aToken, facilitating future governance and reward management.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
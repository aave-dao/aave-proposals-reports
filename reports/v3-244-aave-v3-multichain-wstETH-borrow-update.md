# Proposal 244. wstETH Borrow Rate Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=244)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-wsteth-borrow-rate-update/20762)

### Payloads

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xE94794Aaf5a07751801e9eb3f251c52579beD15b)

* Base - [proposal payloads](https://basescan.org/address/0xb1f63cc8D4762d2C826d52838719b322F441C087)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xE517f35c2735501297DD057A2cD43613f723db17)

* zkSync - [proposal payloads](https://era.zksync.network/address/0x30fcA0887Fbd97Fb9deC3BC2dD75792E25893A03)


## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
This publication proposes updating the wstETH Borrow Rate to support the adoption of LRTs across several instances of Aave v3.

### Proposal Creation
Transaction: [0xba6535fb95910f96f16e3f4cbe88114d7c81ffe3a1f4033d612b50806e81822c](https://etherscan.io/tx/0xba6535fb95910f96f16e3f4cbe88114d7c81ffe3a1f4033d612b50806e81822c)
- `proposalId`: 244
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x545174fa1d70c829c27c35badba4e0b72f1121b6493e0dfb7bcdca724b643605

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 72,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 54,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 33,
        },
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 14,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x545174fa1d70c829c27c35badba4e0b72f1121b6493e0dfb7bcdca724b643605",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/244.md)

**Payload Reports**

* Arbitrum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/72.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/54.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/33.md)

* zkSync - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/14.md)


### Technical Analysis
We have confirmed the intended change to the borrow rate was implemented correctly with respect to decimal scaling, 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
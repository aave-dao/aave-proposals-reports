# Proposal 339. Deprecation of Long-tail Assets

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=339)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-deprecation-of-long-tail-assets/22592)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xDE5acDfcdAae270Fd20d4430295411a5A00B412D)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xeb528A0C35Ab09D8232dFECa12eC2faD3dD443a2)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0xd27a6325234809449bC8Fb980b1eB478c9fd8110)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x16cf0559Bfb7200a8b0c12c8a8866DD455Fc8f8D)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
A proposal to adjust parameters to begin/continue the deprecation process for EURS on Polygon, SNX on Core, and LUSD on Arbitrum and OP due to a lack of liquidity and changing risk profiles.

### Proposal Creation
Transaction: [0x9c432ffff939c14c9f1f94a39e25ada29b32f02e55fe5828d028f6dce524565f](https://etherscan.io/tx/0x9c432ffff939c14c9f1f94a39e25ada29b32f02e55fe5828d028f6dce524565f)
- `proposalId`: 339
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xcb1dd7a51c7b81f3f1a5a4e4c1c01112777fa515738745c876938010c8b6be8b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 316,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 122,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 82,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 96,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xcb1dd7a51c7b81f3f1a5a4e4c1c01112777fa515738745c876938010c8b6be8b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/339.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/316.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/122.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/82.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/96.md)


### Technical Analysis
We have verified the risk parameters have changed to the correct amounts.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
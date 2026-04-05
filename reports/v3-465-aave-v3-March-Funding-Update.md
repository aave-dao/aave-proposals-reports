# Proposal 465. March Funding Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=465)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-march-2026-funding-update/24225)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x7405d7F7B1890efc465F52f974093bB146b98d57)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xeF63452e8F6a6914f894f94054a26Bf13764B3f0)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xd51cd2089ED9c1b9345E4ab9D855EB087B77F1be)

* Base - [proposal payloads](https://basescan.org/address/0x2A0384fE3b3a7D60Ef0369d3368a605d04C1CAD1)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates


### Context
This publication presents the March Funding Update, consisting of the following key activities:

Acquire GHO to support runway;
Consolidate assets on Ethereum and,
Create Allowances to support Operations.

### Proposal Creation
Transaction: [0x918c7d060fb2df1e4d7a1af13f76f1e567781bee6a89f28db79332ee438ce13e](https://etherscan.io/tx/0x918c7d060fb2df1e4d7a1af13f76f1e567781bee6a89f28db79332ee438ce13e)
- `proposalId`: 465
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xe0e11faae136f1455f95c2e48a9f733227b259c26af9a59d546d2db74e1fda5a

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 425,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 140,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 117,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 103,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xe0e11faae136f1455f95c2e48a9f733227b259c26af9a59d546d2db74e1fda5a",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/465.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/425.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/140.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/117.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/103.md)


### Technical Analysis
We verified all requested allowance and budget amounts with respect to their specific token decimal precision.

We verified all recipient SAFE addresses (AFC), delegate wallets (TokenLogic), and all cross-chain token and bridge contract addresses.

We reviewed the dynamic ETH sweep logic, confirming the protocol safely captures 100% of idle native ETH from the Collector and routes it through the WETH Gateway to mint aWETH back to the treasury.

We verified the MainnetSwapSteward token budget replenishments and swappable pair permissions, confirming the exact requested amounts and required oracle initializations.

We reviewed the cross-chain bridging architecture, confirming the safe implementation of the direct-push pattern and accurate routing to the respective native L2 gateways on Arbitrum and Polygon.

We validated the payload logic and confirmed execution via Seatbelt, verifying that exact state diffs match the IPFS and ensuring there are no unintended state changes.


The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 449. February 2026 - Funding Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=449)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-february-2026-funding-update/24030)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x6C176CAeb87Fc3ef2C3DAddC8600be780A132197)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates



### Context
This publication presents the February Funding Update, consisting of the following key activities:

Runway: Acquire GHO to support operational runway.
GHO liquidity: Expand Ahab & AFC SAFEs remit to support GHO liquidity.
Operations: Create allowances to support ongoing operations.

### Proposal Creation
Transaction: [0x7ec36b1f40967cdcaf4d8b8f80bed31a6f7ae301c69882ddd6650fa2ab2a7c4e](https://etherscan.io/tx/0x7ec36b1f40967cdcaf4d8b8f80bed31a6f7ae301c69882ddd6650fa2ab2a7c4e)
- `proposalId`: 449
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xb0a156896cd0f4b24828145c34c36201d03241250aacc0c1c4e49174f427fff4

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 404,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xb0a156896cd0f4b24828145c34c36201d03241250aacc0c1c4e49174f427fff4",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/449.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/404.md)


### Technical Analysis
We verified all requested allowance and budget amounts with respect to their specific token decimal precision.

We verified all recipient SAFE addresses (Ahab, AFC, CEX Earn, Aave Liquidity), delegate wallets (`ACI_SAFE`, `TOKEN_LOGIC`), and token contract addresses.  

We reviewed the dynamic ETH sweep logic, confirming the protocol safely captures 100% of idle native ETH from the Collector and routes it through the WETH Gateway to mint aEthWETH back to the treasury.

We verified the `MainnetSwapSteward` token budget replenishments, confirming the exact requested amounts.

We validated the payload logic and confirmed execution via Seatbelt, verifying that exact state diffs match the IPFS and ensuring there are no unintended state changes.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
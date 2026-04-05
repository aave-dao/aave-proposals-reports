# Proposal 467. Umbrella Deficit Updates

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=467)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-revenue-indexed-deficit-offsets-for-umbrella/24000)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xB9Ee1a1F6BA14974E95e5213bB45a5D9b9515a81)

* Ethereum - [proposal payloads](https://etherscan.io/address/0x2a009f074df124E15d89aca07d448e513AE1526f)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates


### Context
Umbrella makes deficit handling explicit and mechanically enforceable. Once a reserve deficit is realized on-chain, the protocol applies a senior, DAO-backed first-loss layer (the deficitOffset) before any impairment is passed through to Umbrella stakers. Conceptually, the deficitOffset is the protocol’s equity buffer: it is the amount of realized loss the DAO is willing to absorb in that reserve before invoking the backstop.

The core issue is not the existence of this equity layer, but its calibration. Today, deficitOffset is not systematically linked to the protocol’s own realized upside from the same liquidation machinery that occasionally generates deficits. This disconnect is notable because liquidation recapture has never been intended as “free revenue” in isolation. Protocol liquidation fees and, more recently, SVR, have always served a dual purpose: they are mechanisms through which the protocol internalizes part of the liquidation surplus, not only to align incentives, but also to strengthen the system’s ability to absorb future losses. In other words, liquidation-linked profitability has always been conceptually part of the protocol’s security and coverage loop; an earnings stream meant to reinforce resilience over time.

This proposal increases the Umbrella Deficit Offset on USDC, USDT, WETH, GHO and covers existing deficit on CRV, ENS, USDC, USDT and WETH.

### Proposal Creation
Transaction: [0x8070ab6ddcde473f172bbd2fd4bfb9dc9f0c2896726dc302f5e0081418caa1d9](https://etherscan.io/tx/0x8070ab6ddcde473f172bbd2fd4bfb9dc9f0c2896726dc302f5e0081418caa1d9)
- `proposalId`: 467
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xb1bfa28afcd0e2021d10affe39974aaf706e7b8db820857cd9ae614074ded36a

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 417,
        },
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 418,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xb1bfa28afcd0e2021d10affe39974aaf706e7b8db820857cd9ae614074ded36a",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/467.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/417.md)

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/418.md)


### Technical Analysis
We have verified the correct deficit offset amounts for USDT, USDC, WETH, and GHO, as well as the deficit elimination caps for CRV and ENS, with respect to decimal precision.

We have confirmed the pre-execution logic correctly transferring the required aTokens from the Aave Collector to the payload contract to fund the deficit coverage.

We have verified the implementation of the bounding functions   
(_getCappedDeficitToCover and _getDeficitEliminationAmount) to strictly protect the treasury from sudden bad debt spikes.

We have verified that the payloads correctly route the execution, using coverDeficitOffset for assets with active slashing configurations (USDT, USDC, WETH) and coverReserveDeficit for assets without (CRV, ENS).

We have verified the proposal logic and validated its execution via seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 500. Certora Concord Equivalence Checker Funding

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=500)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-strengthening-upgrade-safety-concord-equivalence-checker-by-certora/24713)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x1e8c2A788D128cA3d90C2D6a4bFB4994E5AA004E)


## Certora Analysis

### Proposal Types

* :bank: Payment stream

### Context
This proposal funds Aave's participation as a founding sponsor of **Certora Concord**, an open-source bytecode-level equivalence-checking framework that formally verifies that smart-contract and compiler upgrades (compiler bumps, gas optimizations, refactors) preserve protocol behavior. Authored by Certora and implemented by Aave Labs, it requests a **one-time $50,000 grant, paid in GHO**, as part of a co-funded ecosystem initiative ($200k across four sponsors at $50k each, matched by a $200k Ethereum Foundation contribution for a $400k total). The on-chain action is a single GHO transfer from the Aave Collector to Certora's receiver.

- [Governance forum discussion](https://governance.aave.com/t/arfc-strengthening-upgrade-safety-concord-equivalence-checker-by-certora/24713)
- [Snapshot](https://snapshot.org/#/s:aavedao.eth/proposal/0xcf9ca2d7a9b1ee819b6b76f8dae1cdc7fb507e027f044e90d7937b4b264a42c1)

Proposed by creator `0x66a2…73FF` at access level 1.

### Proposal Creation
Transaction: [0xcdf84d2f79c459fa5118ad2c61de5d4ee68de0285ab5516a78e52f852355570f](https://etherscan.io/tx/0xcdf84d2f79c459fa5118ad2c61de5d4ee68de0285ab5516a78e52f852355570f)
- `proposalId`: 500
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x8a79dd7574d9d3483fc17d21e9f94f977deffdb6a7beb2364d208767c5d218ea

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 453,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x8a79dd7574d9d3483fc17d21e9f94f977deffdb6a7beb2364d208767c5d218ea",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/500.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/453.md)


### Technical Analysis
The proposal consists of a **single Ethereum payload** (👻 PayloadsController `0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5`, payload id 453, deployed at `0x1e8c2A788D128cA3d90C2D6a4bFB4994E5AA004E`), `AaveV3Ethereum_CertoraConcordEquivalenceCheckerFunding_20260623`, which inherits `IProposalGenericExecutor` and is executed via a single delegatecall. Its `execute()` performs exactly one action:

```solidity
AaveV3Ethereum.COLLECTOR.transfer(
  IERC20(AaveV3EthereumAssets.GHO_UNDERLYING),
  CERTORA_RECEIVER,            // 0x0F11640BF66e2D9352d9c41434A5C6E597c5e4c8
  FUNDING_AMOUNT               // 50_000e18
);
```

- **Source:** 👻 Aave V3 Ethereum Collector `0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c` (canonical, matches the source-of-truth address book), standard treasury `transfer()`.
- **Token:** `GHO_UNDERLYING` `0x40D16FC0246aD3160Ccc09B8D0D3A2cD28aE6C2f`, 18 decimals → `50_000e18` = 50,000 GHO (≈ $50,000). Correct token identity and decimal precision.
- **Recipient:** `0x0F11640BF66e2D9352d9c41434A5C6E597c5e4c8`, byte-for-byte identical to the address in the AIP/IPFS spec markdown.
- **Globals:** both `CERTORA_RECEIVER` and `FUNDING_AMOUNT` are `constant` — the payload is stateless and delegatecall-compatible.
- **Test suite:** the unit test asserts the exact balance delta — `assertEq(balanceAfter - balanceBefore, proposal.FUNDING_AMOUNT())` (`.t.sol:46`).
- **Seatbelt:** confirms the only effects are the GHO balance changes (Collector −50,000, receiver 0 → 50,000) plus normal PayloadsController bookkeeping; no warnings, no selfdestruct findings, no unexpected state.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
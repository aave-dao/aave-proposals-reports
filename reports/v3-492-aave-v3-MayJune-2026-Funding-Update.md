# Proposal 492. May/June 2026 Funding Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=492)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-may-june-2026-funding-update/25000)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x71092F5F46033EFb60e2203FB8Eb3ADA0bec5a6a)

* Plasma - [proposal payloads](https://plasmascan.to/address/0x4fda3b7dae898134bd9869885790941c16c9235b)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking

### Context
This publication presents the May/June Funding Update, consisting of the following key activities:

Deposit idle ETH on the Collector into the Aave v3 Core instance;
Refresh the MainnetSwapSteward Allowances to support GHO acquisition and runway;
Create an aEthLidoGHO Allowance for the Tydro incentive campaign;
Refresh the AFC aPlaUSDT0 Allowance on Plasma; and,
Pay out bug bounties and reimburse audit costs.

### Proposal Creation
Transaction: [0x58fac26ce83c36283c015533750dcb0322ad3a8142bcc24225422e3f25b6f4f6](https://etherscan.io/tx/0x58fac26ce83c36283c015533750dcb0322ad3a8142bcc24225422e3f25b6f4f6)
- `proposalId`: 492
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0xe0bbdcba0674118b4ada946fa7d64727db5b47d5ecb12c76bfcca22ee5167a92

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 446,
        },
        {
            chain: "9745",
            payloads_controller: "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d",
            payload_id: 29,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xe0bbdcba0674118b4ada946fa7d64727db5b47d5ecb12c76bfcca22ee5167a92",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/492.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/446.md)

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/29.md)


### Technical Analysis

We have verified that the Ethereum payload deposits the Collector's entire native ETH balance into the Aave V3 Core instance via the `WrappedTokenGatewayV3` (`0xd01607c3C5eCABa394D8be377a08590149325722`), minting aEthWETH to the Collector — 273.43 ETH at simulation time; the exact amount is read from the Collector's balance at execution.

We have verified that the Collector approves exactly 5,000,000 aEthLidoGHO (`0x18eFE565A5373f430e2F809b97De30335B3ad96A`) to the Ahab Safe (`0xAA2461f0f0A3dE5fEAF3273eAe16DEF861cf594e`, `MiscEthereum.AHAB_SAFE`) for the Tydro incentive campaign; the payload creates the allowance only — no transfer to the Safe occurs.

We have verified that the MainnetSwapSteward (`0xb7D402138Cb01BfE97d95181C849379d6AD14d19`) token budgets are increased via `increaseTokenBudget()` by exactly 5,000 WETH, 10,000,000 USDT, 10,000,000 USDC, 10,000,000 USDe, 10,000,000 USDS and 5,000,000 DAI, matching the specification table.

We have verified that the Collector transfers 11,655 aEthLidoGHO to TokenLogic (`0xAA088dfF3dcF619664094945028d44E779F19894`) for the GhoRouter audit reimbursement, and 392,746.66 aEthLidoGHO to Aave Labs (`0x1c037b3C22240048807cC9d7111be5d455F640bd`) for audit cost reimbursements, matching the specified amounts and recipients.

We have verified that the bug-bounty payments transfer 7,500 GHO to the security researcher (`0xcC7383b24631d8BfC8571dbF9c81d6D094688628`), 1,100 GHO to the Sherlock researcher (`0x666B8EbFbF4D5f0CE56962a25635CfF563F13161`) and 750 GHO to Immunefi (`0x7119f398b6C06095c6E8964C1f58e7C1BAa79E18`) — exactly 9,350 GHO leaves the Collector's GHO balance. Note that the payments are denominated in GHO while parts of the description reference USDC.

We have verified that on Plasma the Collector (`0x5E2d083417D12d4B0824E14Ecd48D26831F4Da7D`) approves exactly 3,000,000e6 aPlaUSDT0 (`0x5D72a9d9A9510Cd8cBdBA12aC62593A58930a948`) to the Aave Finance Committee Safe (`0x22740deBa78d5a0c24C58C740e3715ec29de1bFa`, `MiscPlasma.AFC_SAFE`), refreshing a fully-consumed allowance (pre-state slot was zero) to the specified 3M budget.

We have verified that no other state changes occur.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
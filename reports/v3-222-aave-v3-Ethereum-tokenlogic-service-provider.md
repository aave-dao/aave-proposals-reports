# Proposal 222. Funding Proposal: TokenLogic Financial Service Provider

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=222)

### Governance Forum Discussions
[Link to forum discussions](https://governance.aave.com/t/arfc-tokenlogic-financial-services-provider/20182)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xcD4912f3EbE0961f753a7D573EeE2a0052aab120)



## Certora Analysis

### Proposal Types
* :moneybag: :receipt: Asset transfers

* :bank: payment stream

### Context
This proposal outlines TokenLogic’s request to renew its engagement with the Aave DAO for another year, starting December 15, 2024. The team aims to provide essential financial services, including treasury management, analytics, GHO adoption initiatives, and protocol optimization, ensuring the Aave ecosystem’s financial health and growth. TokenLogic proposes a $1M funding stream, managed in aEthLidoGHO, to support these activities while advancing key strategic goals. This renewal emphasizes transparency, sustainability, and the development of tools like the Aave Portal to empower informed decision-making within the DAO.

### Proposal Creation
Transaction: [0xedd4a6dea57a74143e5554e906ac233b8a03da34c1526df5304f9827dec5277f](https://etherscan.io/tx/0xedd4a6dea57a74143e5554e906ac233b8a03da34c1526df5304f9827dec5277f)
- `proposalId`: 222
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xafaae4eb897ce4607b1a14855b69fc9adec481136d06a48cfe565b67ef189bc0

**`createProposal()` Parameters**
```
{
    "payloads": [
        {
            "chain": "1",
            "accessLevel": 1,
            "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            "payloadId": 225
        }
    ],
    "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    "ipfsHash": "0xafaae4eb897ce4607b1a14855b69fc9adec481136d06a48cfe565b67ef189bc0"
}
```

### Aave Seatbelt Report
**Proposal Report**
[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/222.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/225.md)


### Technical Analysis
The following checks were conducted to validate the payload, ensuring it aligns with the proposal details:

1. **Address Verification**:
   - **MILKMAN**: Confirmed as `0x060373D064d0168931dE2AB8DDA7410923d06E88` (verified via Etherscan).
   - **PRICE_CHECKER**: Confirmed as `0xe80a1C615F75AFF7Ed8F08c9F21f9d00982D666c` (verified via Etherscan).
   - **GHO_USD_FEED**: Confirmed as `0x3f12643D3f6f874d39C2a4c9f2Cd6f2DbAC877FC` (verified via Etherscan).
   - **TOKENLOGIC_SAFE**: Confirmed as `0x3e4A9f478C0c13A15137Fc81e9d8269F127b4B40` as outlined in the proposal.

2. **Amount Verification**:
   - **GHO Deposit Amount**: `750,000 GHO` (`750_000e18`), matching the proposal.
   - **USDC Withdrawal Amount**: `750,000 USDC` (`750_000e6`), consistent with the proposal.
   - **Stream Amount**: `1,000,000 GHO` (`1_000_000e18`), aligned with the snapshot and forum discussion.

3. **Decimal Checks**:
   - GHO uses 18 decimals (`e18`), and USDC uses 6 decimals (`e6`), consistent with their ERC-20 implementations. The contract's logic adheres to these precisions.

4. **Stream Duration Calculations**:
   - **Stream Duration**: Defined as `365 days`, consistent with the proposal details.
   - **Actual Stream Amount**: `(1,000,000 GHO / 365 days) * 365 days = almiost 1,000,000 GHO`, ensuring the intended total stream matches the proposal.

5. **Backdated Amount Calculation**:
   - Formula: `(ACTUAL_STREAM_AMOUNT * (block.timestamp - STREAM_START_TIME)) / STREAM_DURATION`.
   - This computation ensures fair proration of the stream for the elapsed time since the start date.

6. **Rounding Differences**:
   - **Known and Expected**: Minor rounding differences in the stream amount due to the division of tokens over the duration are anticipated and acceptable. These differences are intentional and do not impact the overall proposal objectives.

7. **Cross-Validation with Proposal**:
   - All parameters, including addresses, amounts, decimals, and calculations, align with the [snapshot](https://snapshot.box/#/s:aave.eth/proposal/0xd1fdca5d69b03ed57848180d62a812ab1a1ff72f85d671c417b5ff8fb2bd0a7c) and [forum discussion](https://governance.aave.com/t/arfc-tokenlogic-financial-services-provider/20182).


The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
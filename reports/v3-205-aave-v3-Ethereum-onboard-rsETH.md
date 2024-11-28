# Proposal 205. Onboard rsETH to V3 Ethereum


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=205](https://vote.onaave.com/proposal/?proposalId=205)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-rseth-to-aave-v3-ethereum/17696/17](https://governance.aave.com/t/arfc-add-rseth-to-aave-v3-ethereum/17696/17)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3Cca65e2b22a58244d67a5a4638fAC609C1f04E4#code)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

:wrench: :bar_chart: configuration update

<br>

### Context

The proposal seeks to onboard rsETH, a liquid restaking token from KelpDAO, to Aave V3 on Ethereum. KelpDAO is a leading protocol in the EigenLayer ecosystem, offering users benefits such as staking rewards, restaking rewards, and DeFi yields. Adding rsETH to Aave would allow users to leverage these benefits while accessing Aave’s lending and borrowing markets, enhancing utility and liquidity for the token. Additionally, the proposal includes strategic adjustments like e-mode parameters and borrow caps to ensure robust risk management for this integration.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xaf8be8fbe836e91da19d112eee8436a572dea8bac55996107a52246bdcf32500](https://etherscan.io/tx/0xaf8be8fbe836e91da19d112eee8436a572dea8bac55996107a52246bdcf32500)

```
- proposalId: 205
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xf0d9f8887e02bf1657158543b7ff83be7be32aec78b1193364a4d4f8ead9d772
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "210" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xf0d9f8887e02bf1657158543b7ff83be7be32aec78b1193364a4d4f8ead9d772" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/205.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/205.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/210.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/210.md)


<br>

### Technical analysis

The proposal was reviewed with a focus on its configurations, implementation details, and operational correctness. Below is a detailed analysis of its technical components:

#### Configuration Validation

All risk parameter configurations specified in the IPFS documentation were cross-referenced with the Solidity payload, confirming correctness. Key parameters such as LTV (72%), Liquidation Threshold (75%), and Reserve Factor (15%) were appropriately scaled and matched their respective values in the code (e.g., 72_00, 75_00, 15_00). Additionally, caps for rsETH were configured correctly with a Supply Cap of 19,000 and Borrow Cap of 1,900, and both values align with the payload.

#### Emission Manager Configuration

The Emission Manager was correctly configured to assign administrative control for emissions of both the rsETH token and its corresponding aToken. Specifically:
	•	The rsETH address (0xA1290d69c65A6Fe4DF752f95823fae25cB99e5A7) and its corresponding aToken address (retrieved using the AAVE_PROTOCOL_DATA_PROVIDER) were appropriately assigned to the emission admin (0xac140648435d03f784879cd789130F22Ef588Fcd).
	•	Verification of the aToken address retrieval logic showed that the correct aToken address was fetched via the getReserveTokensAddresses function from the protocol data provider.

#### Seed Deposit Verification

The payload includes a seed deposit of 0.04 rsETH (represented as 4e16 in the code) to the pool. This seed deposit ensures liquidity is established for the new token and mitigates the first-deposit attack vector. The deposit is executed by transferring the amount to the Aave Collector contract using the supply function of the Aave pool. The implementation of this step was verified and found to be functional and sufficient, given the token’s expected adoption.

### Conclusion

The technical implementation of the proposal is sound, with all configurations accurately reflected in the payload. The emission manager was properly configured for both the token and its aToken. The seed deposit is sufficient to initiate liquidity in the new pool and was correctly transferred from the Aave Collector.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


# Proposal 210. September Funding Update - Part A


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=210](https://vote.onaave.com/proposal/?proposalId=210)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-september-funding-update/19162](https://governance.aave.com/t/arfc-september-funding-update/19162)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xC554058d890d7faaa98A55649fbE9E727ff74C18#code)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x44E02610ad4ae33d7D199E51e982201C5E389c3A)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x22765bC8B8997d24d47282FaB164279eDd9a39Ed#code)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x24C5ae65Ec7921F6F8A5Be79D458000250E5A89b#code)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal focuses on optimizing the Aave DAO’s treasury by migrating assets from Aave v2 to v3, enhancing efficiency and benefiting from the latest protocol improvements. It includes rescuing funds that are currently locked in Paraswap adapter contracts on Ethereum, ensuring these assets are safely returned to the treasury. The proposal also involves swapping specific stablecoin holdings—such as DAI, FRAX, and LUSD—into GHO to support the DAO’s funding requirements. Additionally, it sets up allowances for the Merit and Ahab programs to facilitate their ongoing operations. Overall, these actions are part of a strategic effort to rebalance the treasury and strengthen the DAO’s financial position.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6787d81876866f6dbfce90e5f1bda191ed9b17e1849149a81c64985c2fb56dbb](https://etherscan.io/tx/0x6787d81876866f6dbfce90e5f1bda191ed9b17e1849149a81c64985c2fb56dbb)

```
- proposalId: 210
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xe931c8b1a1b1cc343762f5eaae5825d9298c21a0c3562279a289abb6e285d00d
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
      "payloadId": "214" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "91" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "59" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "63" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xe931c8b1a1b1cc343762f5eaae5825d9298c21a0c3562279a289abb6e285d00d" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/210.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/210.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/214.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/214.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/91.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/91.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/59.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/59.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/63.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/63.md)


<br>

### Technical analysis

1. **AaveSwapper Upgrade:**
   - The AaveSwapper contract was upgraded to the implementation at `0xd80f4ce4df649d8d6a88cf365f0560bed9ae688f` to mitigate the vulnerability in Milkman’s fee extraction process.

2. **Gas Rebate to Karpatkey:**
   - **Recipient Address:** `0x818C277dBE886b934e60aa047250A73529E26A99` (Karpatkey)
   - **Amount:** `0.264 ETH`
   - **Verification:** The code correctly transfers the specified amount to the intended recipient, matching the proposal’s details.

3. **Merit and Ahab Programs Allowances:**
   - **SAFE Address:** `0xdeadD8aB03075b7FBA81864202a2f59EE25B312b`
   - **Allowances Set:**
     - `3,000,000 GHO`
     - `800 aEthWETH`
   - **Verification:** Allowances are correctly set to the specified address and amounts, aligning with the proposal.

4. **Swapping Funds to GHO:**
   - **Assets and Amounts:**
     - `aUSDC`: `1,250,000 USDC`
     - `aUSDT`: `1,250,000 USDT`
     - `aEthDAI`: `500,000 DAI`
     - DAI, aDAI, aLUSD, LUSD, FRAX, aFRAX: All available balances (minus minimal amounts)
   - **Price Feeds and Slippage Parameters:** Correctly used for each asset swap.
   - **Verification:** The swaps are executed as intended, with amounts matching those specified in the proposal.

5. **Rescue of Paraswap Funds:**
   - **Contracts Involved:**
     - `DEBT_SWAP_ADAPTER`: `0x6A6FA664D4Fa49a6a780a1D6143f079f8dd7C33d`
     - `REPAY_WITH_COLLATERAL_ADAPTER`: `0x02e7B8511831B1b02d9018215a0f8f500Ea5c6B3`
   - **Tokens Rescued:** `sUSD`, `USDC`, `GHO`
   - **Verification:** The tokens are successfully rescued and transferred to the Aave Collector, as per the proposal.

6. **DAI/FRAX/LUSD Availability:**
   - **Observation:** The payload does not explicitly show where DAI, FRAX, and LUSD are transferred to the Collector before swapping.
   - **Verification Needed:** Confirm if these assets are already held by the Collector or if additional steps are required to acquire them.

7. **Address Verification:**
   - All addresses used correspond to official Aave contracts and assets.
   - **Examples:**
     - **MILKMAN Contract:** `0x060373D064d0168931dE2AB8DDA7410923d06E88`
     - **PRICE_CHECKER:** `0xe80a1C615F75AFF7Ed8F08c9F21f9d00982D666c`
   - **Verification:** Addresses are accurate and legitimate.

8. **Numerical Accuracy:**
   - All numerical values, including amounts and slippage percentages, match those stated in the proposal.
   - **Slippage Settings:** Appropriately set based on the volatility of each asset.

9. **Compliance with Proposal Intentions:**
   - Apart from the unmentioned AaveSwapper upgrade, the payload aligns with the actions specified in the proposal.
   - **Actions Covered:** Gas rebate, allowances for Merit and Ahab programs, asset swaps to GHO, and rescue of Paraswap funds.




<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


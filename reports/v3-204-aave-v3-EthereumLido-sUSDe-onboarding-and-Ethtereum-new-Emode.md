# Proposal 202. Onboard and Enable sUSDe liquid E-Mode on Aave v3 Mainnet and Lido Instances


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=204](https://vote.onaave.com/proposal/?proposalId=204)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-and-enable-susde-liquid-e-mode-on-aave-v3-mainnet-and-lido-instance/19703/3](https://governance.aave.com/t/arfc-onboard-and-enable-susde-liquid-e-mode-on-aave-v3-mainnet-and-lido-instance/19703/3)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4C347475403fA6569421209E8Bef010180BA6C58#code)

* Ethereum Lido - [proposal payloads](https://etherscan.io/address/0x228297bb1a094362088646B45538C1fe80d94Fd3#code)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

:wrench: :bar_chart: configuration update


<br>

### Context

The proposal seeks to enable sUSDe Liquid E-Mode on Aave v3 Mainnet and Lido instances to enhance capital efficiency for borrowers using sUSDe as collateral. By implementing this change, borrowers can borrow larger amounts of other stablecoins against their sUSDe collateral, improving overall capital utilization. 

This is expected to optimize the use of sUSDe within the Aave ecosystem, attracting more liquidity and potentially increasing platform revenue. Additionally, Liquid E-Mode provides more precise control over growth and borrow demand relative to stablecoin liquidity on Aave v3 Mainnet.
<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xef5575108c3bd8795d230e9faef2c8837aeb208a1c70003dea18c739df01d4ba](https://etherscan.io/tx/0xef5575108c3bd8795d230e9faef2c8837aeb208a1c70003dea18c739df01d4ba)

```
- proposalId: 204
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x5b478c28422082555bd734854921398123bb270ed0dc8349aa9c90521fa62a00
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
      "payloadId": "209" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x5b478c28422082555bd734854921398123bb270ed0dc8349aa9c90521fa62a00" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/204.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/204.md)

**Payload reports**

* Ethereum & Lido - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/208.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/209.md)


<br>

### Technical analysis

Our analysis focused on verifying that the smart contract payload (Payload 209) for the Aave v3 Lido and Mainnet instances aligns precisely with the configuration values, intentions, and safety measures as outlined in the proposal description. Below is a summary of the key aspects verified:

#### 1. Configuration Consistency
- We compared each specified configuration parameter in the IPFS proposal against the values implemented in the Solidity payload. This included key parameters such as LTV, Liquidation Threshold, Liquidation Bonus, Reserve Factor, and others.
- **Result**: No discrepancies were found, confirming that all declared values were accurately implemented in the contract payload.

#### 2. E-Mode Settings
- We verified that the E-Mode settings for sUSDe, USDC, and USDS were correctly configured. This included checking that all E-Mode parameters such as LTV, Liquidation Threshold, and Liquidation Bonus match the intended values.
- **Result**: All checks passed without discrepancies, confirming that E-Mode settings are correctly implemented to enhance capital efficiency.

#### 3. First Deposit and Seed Amount
- To mitigate risks of a first deposit attack, we confirmed the inclusion of a `seed amount` for the sUSDe asset. The payload includes a deposit of 100 sUSDe to the Aave pool, which aligns with standard measures to prevent first deposit manipulation.
- **Result**: This safeguard was successfully verified in the payload and simulation.

#### 4. Disabling Isolation Mode on Mainnet
- Isolation mode for sUSDe on Aave Mainnet is explicitly set to be disabled. This is confirmed within the `collateralsUpdates()` function of the mainnet payload, aligning with the proposal’s intention to prevent restrictive borrowing configurations on Mainnet.
- **Result**: Isolation mode is correctly disabled in the payload as intended.

#### 5. Price Oracle Confirmation
- We verified the configured price feed (oracle) for sUSDe within the Lido instance. The specified oracle address `0xb37aE8aBa6C0C1Bf2c509fc06E11aa4AF29B665A` matches the intended configuration and ensures accurate pricing for collateral assessments.
- **Result**: The correct oracle is set in the payload.

#### 6. Emission Admin Configuration
- The `Emission Admin` address for sUSDe is configured as `0xac140648435d03f784879cd789130f22ef588fcd`. We confirmed this address is set correctly in both the simulation results and the contract payload, ensuring appropriate administrative control over emission settings for sUSDe.
- **Result**: Emission admin address is correctly configured.

---

### Conclusion
All checks confirmed that the payload accurately reflects the proposal's intended configuration values, adheres to E-Mode parameters for correct operation, includes protections against first deposit attacks, properly disables isolation mode on Mainnet, and verifies both the price oracle and emission admin configurations. 


<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


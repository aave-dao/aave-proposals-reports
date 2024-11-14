# Proposal 201. PYUSD Reserve Configuration Update & Incentive Campaign


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=201](https://vote.onaave.com/proposal/?proposalId=201)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-pyusd-reserve-configuration-update-incentive-campaign/19573/2](https://governance.aave.com/t/arfc-pyusd-reserve-configuration-update-incentive-campaign/19573/2)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4927022149AAfE0B199722869b9Eb96d1c1799cf#code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

:handshake: permission granting or revoking

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal aims to enhance the adoption and liquidity of PayPal’s stablecoin, PYUSD, on the Aave platform. By adjusting the reserve settings for PYUSD and implementing a six-month incentive campaign, it seeks to make PYUSD borrowing more attractive, offering up to 4% APR in rewards for Aave users. Additionally, a liquidity pool on Balancer is proposed to support PYUSD/GHO trading, with further incentives provided by PayPal and Trident Digital. This dual effort is intended to increase PYUSD’s utility and improve its liquidity, making it a more viable asset within DeFi.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x2038734975b9e5407ceb1417d5d8dff4fc25c8abad9d641a526171f5edc4aced](https://etherscan.io/tx/0x2038734975b9e5407ceb1417d5d8dff4fc25c8abad9d641a526171f5edc4aced)

```
- proposalId: 201
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x60f540e34c1b586a245dc16025098ca382fde4d9cb104a8c04a39745f3a7ea81
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
      "payloadId": "207" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x60f540e34c1b586a245dc16025098ca382fde4d9cb104a8c04a39745f3a7ea81" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/201.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/201.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/207.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/207.md)

<br>

### Technical analysis

We have verified that the proposal payload does the following:

1. **Adjusts PYUSD Reserve Parameters on Aave v3:**
   - **Borrow Cap**: Sets the borrow cap for PYUSD to 15 million.
   - **Loan-to-Value (LTV)**: Configures LTV at 75%.
   - **Liquidation Threshold (LT)**: Sets LT to 78%.
   - **Liquidation Penalty**: Establishes a liquidation penalty of 7.5%.
   - **Liquidation Protocol Fee**: Applies a 10% liquidation protocol fee.

2. **Approves a 300,000 GHO Allocation to the Aave Liquidity Coordinator (ALC SAFE):**
   - Enables the Aave Collector to approve 300,000 GHO to the ALC SAFE address, facilitating liquidity support for the PYUSD/GHO pool on Balancer. 
3. **Sets Emission Admin Rights for PYUSD and aEthPYUSD:**
   - Grants `ACI_TREASURY` control over emissions for both PYUSD and aEthPYUSD.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


# Proposal 293. April Funding update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=293)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-april-funding-update/21590)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x559A4707dB33B28C2c2e9f83A5f205a164F02191)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x5F876Db887658c29a9772AFbA54d65B83a9AB079)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers

* :wrench: :bar_chart: Configuration updates


### Context
This publication presents the April Funding Update, consisting of the following key activities:

- Bridge funds to Ethereum;
- Fund Sonic incentive campaign;
- Acquire GHO for Operations; and,
- Transfer FLUID to Aave Protocol Embassy.
- Fund to [CrossChainController](https://etherscan.io/address/0xEd42a7D8559a463722Ca4beD50E0Cc05a386b0e1)
- Update stataUSDT GSM Exposure Cap as it has successfully drawn swaps from aggregators

### Proposal Creation
Transaction: [0x2cac2bd922ab31bc721112508dfa486b31559aeece2bb9ebb4a863949d0a4131](https://etherscan.io/tx/0x2cac2bd922ab31bc721112508dfa486b31559aeece2bb9ebb4a863949d0a4131)
- `proposalId`: 293
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x87a8aaaa34d0fbe1b588b7560fbf28d5bcff95417037e20f3529b79a3ae412ad

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 270,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 109,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x87a8aaaa34d0fbe1b588b7560fbf28d5bcff95417037e20f3529b79a3ae412ad",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/293.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/270.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/109.md)


### Technical Analysis
- **Polygon Bridge Details**:  
  - Verified that the assets queued for bridging from Polygon to Ethereum are exactly:  
    - `USDC.e`  
    - `USDT`  
    - `WETH`  
    - `DAI`  

- **GHO Acquisition on Ethereum**:  
  - Confirmed that the swap and deposit procedures are set to target:  
    - **2.00M aUSDT**  
    - **2.00M aUSDC**  

- **Aave Protocol Embassy & Sonic Incentives**:  
  - **FLUID Transfer**:  
    - Checked that the FLUID asset is being transferred to the Aave Protocol Embassy SAFE at the specified address:  
      - `0xa9e777D56C0Ad861f6a03967E080e767ad8D39b6`
  - **Sonic Incentive Allowance**:  
    - Verified the allocation of **0.8M aEthUSDC** as an allowance to fund the Sonic Incentive Campaign from the Aave v3 Core instance to the appropriate Merit address, corresponding with the specified operational design.

- **CrossChainController Funding**:  
  - Ensured that the funding mechanism to the CrossChainController includes the correct transfer amounts:  
    - **50 LINK**  
    - **1 native ETH**  
  - Confirmed that this transaction is directed to the mainnet address:  
    - `0xEd42a7D8559a463722Ca4beD50E0Cc05a386b0e1`

- **GSM Exposure Cap Update**:  
  - Validated that the proposal correctly updates the stataUSDT GSM exposure cap to **25M units**.


The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
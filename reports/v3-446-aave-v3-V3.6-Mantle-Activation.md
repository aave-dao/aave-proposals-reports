# Proposal 446. Aave V3.6 Mantle Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=446)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-deploy-aave-v3-on-mantle/20542/12)

### Payloads



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets


### Context
This proposal allows the Aave governance to activate the Aave V3 Mantle pool (3.6) by completing all the initial setup and listing WETH, WMNT, USDT0, USDC, USDe, sUSDe, FBTC, syrupUSDT, wrsETH as suggested by the risk service providers engaged with the DAO on the governance forum.


### Proposal Creation
Transaction: [0xf4fab988e6d48509ce3b7d06855960daa46ccf4dc2ea09d671e414aa5d51c0c7](https://etherscan.io/tx/0xf4fab988e6d48509ce3b7d06855960daa46ccf4dc2ea09d671e414aa5d51c0c7)
- `proposalId`: 446
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x698854457f13a3710f67de8d7cd48e44fbb897a9ee047771a848599695a3787b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "5000",
            payloads_controller: "0xF089f77173A3009A98c45f49D547BF714A7B1e01",
            payload_id: 2,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x698854457f13a3710f67de8d7cd48e44fbb897a9ee047771a848599695a3787b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/446.md)

**Payload Reports**


### Technical Analysis
We verified seed amounts with respect to token decimal precision.  
We verified token addresses, Chainlink price feed addresses, and all risk parameters.  
We reviewed all E-Mode categories and their configurations.    
The payload follows the independent E-Mode tables, which were inconsistent with the large aggregated table. We discussed this with BGD for clarification, and they updated the table.  
We confirmed that, for the newly listed assets, both LTV and liquidation threshold are set to 0. Except `WETH` and `WMNT`.  
We validated the payload logic and confirmed execution via Seatbelt.


The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
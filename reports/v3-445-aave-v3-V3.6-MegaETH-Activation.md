# Proposal 445. Aave V3.6 MegaETH Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=445)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-deploy-aave-v3-to-megaeth/23517)

### Payloads

* MegaETH - [proposal payloads](https://megaeth.blockscout.com/address/0x3a0A755D940283cD96D69F88645BeaA2bAfBC0bb)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets


### Context
This proposal allows the Aave governance to activate the Aave V3 MegaETH pool (3.6) by completing all the initial setup and listing WETH, BTCb, USDT0, USDm, wstETH, wrsETH, ezETH as suggested by the risk service providers engaged with the DAO on the governance forum.


### Proposal Creation
Transaction: [0xaced4eb0667a068278bb606360424435e52ade5f8f20ff4b964a3bfc2cb9eee0](https://etherscan.io/tx/0xaced4eb0667a068278bb606360424435e52ade5f8f20ff4b964a3bfc2cb9eee0)
- `proposalId`: 445
- `creator`: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- `accessLevel`: 1
- `ipfsHash`: 0xec9fb2abca293ea0abbebe3f87a6d0afee08be966a231d2eec67ec434ab7d814

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "4326", 
      "accessLevel": "1", 
      "payloadsController": "0x80e11cB895a23C901a990239E5534054C66476B5", 
      "payloadId": "0" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0xec9fb2abca293ea0abbebe3f87a6d0afee08be966a231d2eec67ec434ab7d814" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/4326/0x80e11cB895a23C901a990239E5534054C66476B5/0_forge.md)

**Payload Reports**

* MegaETH - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/4326/0x80e11cB895a23C901a990239E5534054C66476B5/0_forge.md)


### Technical Analysis

We verified seed amounts with respect to token decimal precision.  
We verified token addresses, price feed addresses (Chainlink), and all risk parameters.  
We reviewed all eMode categories and their configurations.  
We confirmed that for the newly listed assets, LTV and liquidation threshold are set to 0.  
We validated the payload logic and confirmed execution via Seatbelt.
 
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
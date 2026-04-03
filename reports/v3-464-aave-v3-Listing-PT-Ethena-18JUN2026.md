# Proposal 464. Listing PT Ethena 18JUN2026


### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=464)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-usde-susde-june-expiry-pt-tokens-on-aave-v3-plasma-instance/24304/3)

### Payloads

* Plasma - [proposal payloads](https://plasmascan.to/address/0xBe797B92510EfBf8Cd10e2C34c2F98571963f010#code)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :gem: :new: Listing new assets
* :wrench: :bar_chart: Configuration updates


### Context
This AIP proposes to onboard USDe and sUSDe June expiry PT tokens on Aave V3 Plasma Instance.

### Proposal Creation
Transaction: [0x08888d74a09504c9b27f0bd995ed2f3a60d4eca89ae030d353d8ce96c4215f4b](https://etherscan.io/tx/0x08888d74a09504c9b27f0bd995ed2f3a60d4eca89ae030d353d8ce96c4215f4b)
- `proposalId`: 464
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x0c2674682c2bf4b4c1f4b71f9d4eab67d5225916c1d0226aa780bffa8fa0785e

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "21" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0x0c2674682c2bf4b4c1f4b71f9d4eab67d5225916c1d0226aa780bffa8fa0785e" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/464.md)

**Payload Reports**

* Plasma - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/21.md)


### Technical Analysis

We have confirmed the new listing of `PT Ethena USDe 18JUN2026` and `PT Ethena sUSDE 18JUN2026` with the correct parameters, and verified the seed amount with respect to decimal precision.

We have verified that id = 1 maps to `PendleDiscountRateUpdate` on AgentHub.

Additionally, `0xac140648435d03f784879cd789130F22Ef588Fcd` is set as the emission admin for the tokens and the corresponding aToken and vToken.

We have checked the price feed for the newly listed tokens.

We have verified the creation of the new E-modes with the correct risk parameters.

We have verified proposal logic and validate its execution via seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
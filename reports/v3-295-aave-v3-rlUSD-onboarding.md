# Proposal 295. Add rlUSD to Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=295)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-add-rlusd-to-core-instance/20214)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xc855D3935dB5F181EE873d70aD97013C1899Dc4d)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This AIP seeks governance approval to onboard Ripple’s rlUSD stablecoin to the Core instance of Aave v3 on Ethereum.

### Proposal Creation
Transaction: [0x3a546dcb56a771b2fe2d2449b0291a23cda9137a232357674aa9171b241e0bf8](https://etherscan.io/tx/0x3a546dcb56a771b2fe2d2449b0291a23cda9137a232357674aa9171b241e0bf8)
- `proposalId`: 295
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x7bf5753a0e909b4256fc406e6e6897cafebfcb8e0179e2e9696650ac0c6f7226

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 272,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x7bf5753a0e909b4256fc406e6e6897cafebfcb8e0179e2e9696650ac0c6f7226",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/295.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/272.md)


### Technical Analysis
We have compared the risk parameters between the ipfs to the payload, we have identified the price feed and made sure the seed supply configured correctly.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
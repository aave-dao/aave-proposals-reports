# Proposal 402. Security Services for Aave Current Infrastructure <> Certora

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=402)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-security-services-for-aave-current-infrastructure-certora/23221)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xfC33e11460655E62160286166fdAeA4e3C23C665)



## Certora Analysis

### Proposal Types

* :bank: Payment stream

### Context
This AIP will open a one year aLidoGHO stream of 238,000$ to compensate Certora for their future work on the currently deployed Aave infrastructure.

### Proposal Creation
Transaction: [0xd0dec724417f11f7335a59424708065ce1db951ffa9e02605139badebfc2d537](https://etherscan.io/tx/0xd0dec724417f11f7335a59424708065ce1db951ffa9e02605139badebfc2d537)
- `proposalId`: 402
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xb781cb7aa347dc7e27c4d6f3a0bc222fee77ad21ff4c9260d20c6aee0ca0bf10

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 365,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xb781cb7aa347dc7e27c4d6f3a0bc222fee77ad21ff4c9260d20c6aee0ca0bf10",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/402.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/365.md)


### Technical Analysis
We confirmed alignment between the forum post, IPFS, and the on-chain payload, including verification of the intended Certora recipient address. The payload’s behavior was validated through Seatbelt’s simulated execution environment, which confirmed that it initializes the expected 365-day aLidoGHO payment stream with no irregularities. All checks are consistent with the proposal specification.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
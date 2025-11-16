# Proposal 403. Security Services for Aave v4 <> Certora

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=403)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-security-services-for-aave-v4-certora/23222)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x55EEAf7306A17d408192C3d4A9b5799E4a810cB9)



## Certora Analysis

### Proposal Types


* :bank: Payment stream

### Context
This AIP will create a one year stream of 2,390,000$ aLidoGHO to Certora to compensate them for their future work on Aave V4.

### Proposal Creation
Transaction: [0xc4b8233f30863dde0b94ff2bc5b0b9dc414337eb7b2ff133cdea1ebd57b422d2](https://etherscan.io/tx/0xc4b8233f30863dde0b94ff2bc5b0b9dc414337eb7b2ff133cdea1ebd57b422d2)
- `proposalId`: 403
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x91c33eb3ff7eb538c9b4add1059af4515cbf477e66e5f478c611479887834278

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 366,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x91c33eb3ff7eb538c9b4add1059af4515cbf477e66e5f478c611479887834278",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/403.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/366.md)


### Technical Analysis
We verified alignment between the forum post, IPFS, and the on-chain payload, including confirmation of the designated Certora payment-stream address. Seatbelt’s simulated execution confirms that the payload initializes the expected one-year aLidoGHO payment stream with no deviations from the specification. No inconsistencies or anomalies were detected across any reference sources.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
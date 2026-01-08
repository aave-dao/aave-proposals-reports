# Proposal 430. Orbit Program Renewal - Q1 and Q2 2026

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=430)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-orbit-program-renewal-q1-and-q2-2026/23695)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xA0A636EAd5c1E28B9ceb88976792908B6e4f917B)



## Certora Analysis

### Proposal Types

* :bank: Payment stream

### Context

Proposing the latest renewal of the Orbit program for recognized delegates, compensating them with GHO, associated with their future governance activity during Q1 and Q2 2026( From 2026-01-01 new date when [ARFC] Orbit Program Renewal - Q3 and Q4 2025 ends, until 2026-06-30).



### Proposal Creation
Transaction: [0x8a0eacb7ba98d08b68432544f9cdc0748613365b30514300e0c701f4c0c3a4af](https://etherscan.io/tx/0x8a0eacb7ba98d08b68432544f9cdc0748613365b30514300e0c701f4c0c3a4af)
- `proposalId`: 430
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x85b3f3aadd693ccc0035a629d3988d5e883f811a64057d421787ca32ea65df6f

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 391,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x85b3f3aadd693ccc0035a629d3988d5e883f811a64057d421787ca32ea65df6f",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/430.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/391.md)


### Technical Analysis

We have verified the recipient addresses and stream amounts:

* `EZREAL` — 60,000 (aEthLidoGHO)
* `StableLab` — 30,000 (aEthLidoGHO)
* `IgnasDefi` — 30,000 (aEthLidoGHO)
* `Areta` — 30,000 (aEthLidoGHO)

We confirmed that the stream end date matches what’s described in the forum and IPFS.

We validated the payload logic and execution, and verified it via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
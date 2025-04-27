# Proposal 297. Renew LlamaRisk as Risk Service Provider - epoch 3

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=297)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-renew-llamarisk-as-risk-service-provider-epoch-3/21666)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x1883A10602464B55b48e536E3a41c5fe40d5f9aF)



## Certora Analysis

### Proposal Types

* :bank: Payment stream

### Context
This proposal renew LLamaRisk engagement as a service provider for a year.

### Proposal Creation
Transaction: [0x1c3ad1c8b4e46e1658b6517d2b27a7c643d6548ca5b19233e64b8631654aebce](https://etherscan.io/tx/0x1c3ad1c8b4e46e1658b6517d2b27a7c643d6548ca5b19233e64b8631654aebce)
- `proposalId`: 297
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xd32df20fa05a83069390916edd23f8e46ae215fcc9713fa8bcf4df5b1e09e765

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 277,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xd32df20fa05a83069390916edd23f8e46ae215fcc9713fa8bcf4df5b1e09e765",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/297.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/277.md)


### Technical Analysis
We have verified that the amount that was approved is the actual amount that was streamed (with respect to precision). We have verified the address and the duration of the stream.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
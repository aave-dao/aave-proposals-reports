# Proposal 454. ACI Is Leaving Aave

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=454)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-aci-stream-settlement/24206)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xb942e9DE879117a05d4d531940217b1A97a5BF93)



## Certora Analysis

### Proposal Types


* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking
* :bank: Payment stream

### Context
Cancel ACI’s GHO stream (ID 100070) on the Aave Collector and transfer 120 days worth of stream to treasury.aci.eth. The remaining balance returns to the Collector.

ACI is departing the Aave DAO. The full context is in our [departure post](https://governance.aave.com/t/aci-is-leaving-aave/24205).

### Proposal Creation
Transaction: [0x68f000587ae54693dc82ecac57d6b5b30c69d0edce76d05a7da4e2179b6eced9](https://etherscan.io/tx/0x68f000587ae54693dc82ecac57d6b5b30c69d0edce76d05a7da4e2179b6eced9)
- `proposalId`: 454
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x695a1cc44834be06934559d8d0d79c35eabf87ea5749f4f7910195dc81ed9e40

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 410,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x695a1cc44834be06934559d8d0d79c35eabf87ea5749f4f7910195dc81ed9e40",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/454.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/410.md)


### Technical Analysis
We confirmed the complete teardown of Stream `100070`. The CancelStream event executed correctly, zeroing out the internal _streams mapping for this ID.

We verified that upon cancellation, the accrued recipientBalance of `113,632.32 aEthLidoGHO` was accurately transferred to ACI's treasury.

We confirmed that the unvested, remaining balance of `2,039,940 aEthLidoGHO` was successfully refunded and safely remains with the Aave Collector.

We have verified proposal logic and validate its execution via seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
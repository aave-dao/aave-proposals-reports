# Proposal 229. Funding Proposal: karpatkey as GHO Growth Service Provider

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=229)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-karpatkey-as-gho-growth-service-provider/20206)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x0a2A9a20F42e663f4fdC94eE7dA1B0E245D87C1D)


## Certora Analysis

### Proposal Types

* :bank: Payment stream

### Context
The AIP proposes appointing karpatkey as a service provider dedicated to drive the growth of GHO for the following 6 months, with an initial focus on opportunities within the Gnosis Chain while also expanding efforts to other chains.

### Proposal Creation
Transaction: [0xf4971f635f0c923094ec2085c0ee62999b0d0fe39009913d529eedd6c8a364ce](https://etherscan.io/tx/0xf4971f635f0c923094ec2085c0ee62999b0d0fe39009913d529eedd6c8a364ce)
- `proposalId`: 229
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x9a9652b1de57a9e14c6897ffa831333f6f22889ebe18381ddcadc66b5b34ab4e

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 231,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x9a9652b1de57a9e14c6897ffa831333f6f22889ebe18381ddcadc66b5b34ab4e",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/229.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/231.md)


### Technical Analysis
We have verified that the address to whom the stream is approves is indeed Karpetkey. We have verified that the duration calculation is correct and that the starting time is as intended.


The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
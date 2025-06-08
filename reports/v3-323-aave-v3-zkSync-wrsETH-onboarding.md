# Proposal 323. Onboard wrsETH to ZKsync V3 Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=323)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-wrseth-to-zksync-v3-instance/20727)

### Payloads

* zkSync Era - [proposal payloads](https://era.zksync.network/address/0x7BCF4Cc0A26f9BC38AD26A1c923A3C25E210f608)

* Ethereum - [proposal payloads](https://etherscan.io/address/0xCbAda2F047b2835dC3B879b11700577a074d6587)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

* :gem: :new: Listing new assets


### Context
This is a proposal to onboard wrsETH to the Aave V3 ZKsync Instance allowing Aave users to supply wrsETH as collateral. This proposal will be under Direct to AIP, as there are already on other Aave Instances.

Additionally, this AIP will update the rsETH LST E-Mode of the Prime instance.


### Proposal Creation
Transaction: [0xfeff64c3ea24cb64311a88cec8e6d67b8114397cb9dff941e3b03edbb8e02a6b](https://etherscan.io/tx/0xfeff64c3ea24cb64311a88cec8e6d67b8114397cb9dff941e3b03edbb8e02a6b)
- `proposalId`: 323
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x9638f94b66a2364fea5fd11606328a1994720255a0aaa54d90746b332947b41b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 27,
        },
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 298,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x9638f94b66a2364fea5fd11606328a1994720255a0aaa54d90746b332947b41b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/323.md)

**Payload Reports**

* zkSync Era - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/27.md)

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/298.md)


### Technical Analysis
We have validated the seed amount is supplied to the executor. We have verified the price feed. We have compared the risk parameters to the specified numbers in the IPFS.
The seatbelt report was reverted due to unrelated technical issue on the zkSync seatbelt. The foundry report ran successfully thus the proposal is approved.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
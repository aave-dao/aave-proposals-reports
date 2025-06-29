# Proposal 328. Aave V3 Aptos Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=328)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-v3-deployment-on-aptos-mainnet/21823)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x48Bc64e2B966280A727CCC2F424a1A40126EFF0C)



## Certora Analysis

### Proposal Types
* :scroll: :small_red_triangle: Contract upgrades

* :handshake: Permission granting and revoking

* :gem: :new: Listing new assets


### Context
This proposal seeks to formally approve the already-deployed Aave V3 Aptos Market under the Aave DAO, marking Aave’s first expansion into a non-EVM blockchain. Bringing the Aptos market under DAO will leverage Aptos’s high throughput, low transaction fees, and the Move programming language’s security features to enhance Aave’s protocol performance and broaden its user base.

### Proposal Creation
Transaction: [0xce1f49c2ee39db920b39847ccafa5f63bdcd6ae86e98576b1cea14f31ba5de6c](https://etherscan.io/tx/0xce1f49c2ee39db920b39847ccafa5f63bdcd6ae86e98576b1cea14f31ba5de6c)
- `proposalId`: 328
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x655034112ecc3f89cbcfc7420c490928d01772bcae507a954f1f26be02b4687b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 305,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x655034112ecc3f89cbcfc7420c490928d01772bcae507a954f1f26be02b4687b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/328.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/305.md)


### Technical Analysis
We have verified the listed assets on Aptos were configure with the correct risk parameters (LTV 0 is correct although not specified). The contracts code match the v3.3 special Aptos implementation.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
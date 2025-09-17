# Proposal 370. September Funding Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=370)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-september-2025-funding-update/22915)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x231CDf25D96B97b9FED9E081e99F079fa8d998eE)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x7e374bd2B6C7a4DA694bD736e9B17c5Aa1a812b5)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x17720d859EDC20333BDD53735640680F2AFA4612)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x32ebf9cdc588D054b728692d60A9f73F725099b3)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xFC5D15F348C0f33D88411302121439854945Ae17)

* Sonic - [proposal payloads](https://sonicscan.org/address/0xCa0582912C076828C778090ddB4A393E4C5613dC)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers

* :handshake: Permission granting and revoking



### Context
This publication presents the September Funding Update, consisting of the following key activities:

Bridge funds to Ethereum; Create 2M USD Allowance for AAVE buybacks; Consolidate asset holdings; and, Create Allowances to support Operations.


### Proposal Creation
Transaction: [0xe49775e0949c13b0174b19416dac2eb16bfd38481180530b980d9b42862a4b1a](https://etherscan.io/tx/0xe49775e0949c13b0174b19416dac2eb16bfd38481180530b980d9b42862a4b1a)
- `proposalId`: 370
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xc119cd91d013699f33f2be705858eb1e0c963b60ba402959758348d412776b54

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 338,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 127,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 85,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 102,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 61,
        },
        {
            chain: "146",
            payloads_controller: "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695",
            payload_id: 9,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xc119cd91d013699f33f2be705858eb1e0c963b60ba402959758348d412776b54",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/370.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/338.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/127.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/85.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/102.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/61.md)

* Sonic - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/146/0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695/9.md)


### Technical Analysis
We have verified the amounts are correct throughout the proposal, with respect to decimal precision. We have verified the logic of the Milkman swap to be correct. We have matched the addresses presented in the payloads to the forum and the respective source of truth. We located and discussed parts which were omitted form the payload itself but are presented in the forum post.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
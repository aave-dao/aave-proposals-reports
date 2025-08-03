# Proposal 349. July 2025 - Funding Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=349)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-july-2025-funding-update/22555)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x5E8c1b07081635d2e7F8BA1e10265c26B9492f4A)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xF452F9035434c5A59D6BCc32F882617F86FE2Fb0)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x193169Da8C556739aEbB519a486C008f481f0c04)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x70A7ACa1be32363F4bfC1402CbCD63bA6C2F2220)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers

* :handshake: Permission granting and revoking

* :bank: Payment stream

### Context
This proposal presents the July Funding Update, consisting of the following key activities:

- Bridge funds to Ethereum from Arbitrum and Polygon;
- Extend EURe incentive campaign and,
- Swap LUSD, PYUSD and DAI to USDC.
- Gas costs reimbursement to ACI.
- Orbit renewal program.
- Continue AAVE Buybacks for 4 weeks.

### Proposal Creation
Transaction: [0xa3d6ba7be08bf3cc013b8f9bc622cb59acb3006b1d7c969d050e830a822a163f](https://etherscan.io/tx/0xa3d6ba7be08bf3cc013b8f9bc622cb59acb3006b1d7c969d050e830a822a163f)
- `proposalId`: 349
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x81e75ea2158fec9701b158228f8224684ba13ac669b0bd70c6f07f75a7807fc2

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 322,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 125,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 98,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 58,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x81e75ea2158fec9701b158228f8224684ba13ac669b0bd70c6f07f75a7807fc2",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/349.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/322.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/125.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/98.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/58.md)


### Technical Analysis
All recipient addresses and amounts (to the required precision) have been verified, with no modifications made to the IPFS data.

 The proposal aligns with the descriptions provided on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
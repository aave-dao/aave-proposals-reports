# Proposal 413. November Funding Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=413)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-november-2025-funding-update/23339)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xDd4Ab96b7E97cD121b772c59E897A343d83D797e)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x8Da49c8C52DB89e9e0A3D31bFC0c971A3e20013c)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x792A56f4b14c0c70a963F5E33e55Eb527dA875fE)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0xE32D1C628d79ED98d6D1D76bdc2898B02c6F49d4)

* Sonic - [proposal payloads](https://sonicscan.org/address/0x26cF7Ec116037447cc138348b1983Ff935128009)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking

### Context
This publication presents the November Funding Update, consisting of the following key activities:

* Bridge funds to Ethereum;
* Acquire GHO to support runway;
* Consolidate asset holdings; and,
* Create Allowances to support Operations.

### Proposal Creation
Transaction: [0x62cee32128d8a1e974a69530018644b7bd99593d7e935943e3380edba2ec6dc3](https://etherscan.io/tx/0x62cee32128d8a1e974a69530018644b7bd99593d7e935943e3380edba2ec6dc3)
- `proposalId`: 413
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x5294682fc73e176110098798f21b5ce3e8d9ee98fbffe266543741e07d2ee31a

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 373,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 133,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 88,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 51,
        },
        {
            chain: "146",
            payloads_controller: "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695",
            payload_id: 11,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x5294682fc73e176110098798f21b5ce3e8d9ee98fbffe266543741e07d2ee31a",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/413.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/373.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/133.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/88.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/51.md)

* Sonic - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/146/0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695/11.md)


### Technical Analysis

We have verified assets addresses and amounts with regarding to decimal precision.
We have validate approval logic and initialization of the allowance back to zero before approving. 
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 304. May Funding Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=304)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-may-2025-funding-update/21906)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x143ff8BBF2Ea2f91Cd527087E6AF7f0e21627738)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x2d300D5432eaA0072D9A325d0011721bB7fD8967)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x860e5dAecE99FA8D1e4980b136C38Ab9aF4cfE2B)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x5201aBE940D9082A0c73035364CdAc00BCc0d87C)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xBE5b825a47763e7a11a196cc74045fa965622CF4)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers

* :handshake: Permission granting and revoking



### Context
This publication presents the May Funding Update, consisting of the following key activities:

- Bridge funds to Ethereum;
- Consolidate funds from the Collector;
- Merit, Ahab allowances
- Create 6M USD Allowance for AAVE buybacks; and,
- Acquire 4M GHO for Operations.

### Proposal Creation
Transaction: [0x73caf4f96cc8de5266e064379bc79f0ab02f338deaee90ae94ba414e30e63b28](https://etherscan.io/tx/0x73caf4f96cc8de5266e064379bc79f0ab02f338deaee90ae94ba414e30e63b28)
- `proposalId`: 304
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x242880f29623ea7d22bc19aa9f44c640ed02af1204a86ab3d5fb8c803a2a9059

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 282,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 110,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 74,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 86,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 51,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x242880f29623ea7d22bc19aa9f44c640ed02af1204a86ab3d5fb8c803a2a9059",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/304.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/282.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/110.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/74.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/86.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/51.md)


### Technical Analysis
We identified a minor configuration error in the Ethereum payload: the aEthLidoGHO allowance (GHO_ALLOWANCE_AMOUNT) was set to 3 million using 6 decimals of precision instead of the required 18 decimals. This should be corrected in a follow‑up proposal, but it does not block the current proposal’s execution.

All other parameters, addresses, and procedures align exactly with the IPFS specification and forum discussion.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
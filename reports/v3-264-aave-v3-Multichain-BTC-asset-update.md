# Proposal 264. Core & Base - BTC Correlated Asset Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=264)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-core-base-btc-correlated-asset-update/20940)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xC6aFC85c0FBCc3aaEFE2Dfbf4Ebd5D0B650c6C19)

* Base - [proposal payloads](https://basescan.org/address/0xeF6b41073eA9BD7Afad13f3cEF9fFEE85268Fd58)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
Several initiatives are included:

- Onboard LBTC on Base;
- Create LBTC/cbBTC eMode on Core instance;
- Create LBTC/tBTC eMode on Core instance;
- Create LBTC/cbBTC eMode on Base instance; and;
- Amend cbBTC Borrow Rate.


### Proposal Creation
Transaction: [0x850f43fb1c34ebea491625429f700299e458936d3a902ae9e9d4101031f28e3c](https://etherscan.io/tx/0x850f43fb1c34ebea491625429f700299e458936d3a902ae9e9d4101031f28e3c)
- `proposalId`: 264
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xe8cf37c4fe2b24cbbf6296ff230af6e84185d3749bb8af9c056243bfa1c7188d

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 255,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 58,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xe8cf37c4fe2b24cbbf6296ff230af6e84185d3749bb8af9c056243bfa1c7188d",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/264.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/255.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/58.md)


### Technical Analysis
We have verified that the risk parameters are configured correctly. During the voting phase the executer was yet to be funded  in Base but upon the end of the voting phase it was funded with the needed seed amount.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
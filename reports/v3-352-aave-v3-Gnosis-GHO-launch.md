# Proposal 352. GHO Gnosis Launch

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=352)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-launch-gho-on-gnosis-chain/21379/11?u=kpk)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x6a8EE4997DaE71b825cD09928569Fa64be0eeF70)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x2699985037127B6648325F50f0213C9D2a95Efaa)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x3269C288C9581d9d1Ba44483A18B5d45d5A524D8)

* Base - [proposal payloads](https://basescan.org/address/0xB89C9d76f88028446A7CeF10cFa8E9670d48721C)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x43a1FaEfCaE05164153aD9B6e7bA1209808bB5D4)

* Gnosis 2 - [proposal payloads](https://gnosisscan.io/address/0x63e170c404a17F18D8cD90226117444e5EE510D6)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking

* :gem: :new: Listing new assets


### Context
This AIP proposes the expansion of GHO, the native asset of the Aave Protocol, to the Gnosis Chain network utilizing the Chainlink Cross-Chain Interoperability Protocol (CCIP).

### Proposal Creation
Transaction: [0x1d530d83ffa3ee7008c8456481413d4563a4c22c1b46f8fdb0bf03888dfcb30a](https://etherscan.io/tx/0x1d530d83ffa3ee7008c8456481413d4563a4c22c1b46f8fdb0bf03888dfcb30a)
- `proposalId`: 352
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x1d24f0279264d6d17f5d1e432bfb88a1c755b4e2e5b25f3d58cec9a6ed064aa0

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 324,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 99,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 92,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 83,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 59,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 60,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x1d24f0279264d6d17f5d1e432bfb88a1c755b4e2e5b25f3d58cec9a6ed064aa0",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/352.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/324.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/99.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/92.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/83.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/59.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/60.md)


### Technical Analysis
We have verified the addresses used in the payloads. We have confirmed the logic of the payloads. We have confirmed the risk parameters of the GHO listing is the same as forum and IPFS.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
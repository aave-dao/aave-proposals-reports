# Proposal 240. GHO Base Launch

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=240)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-launch-gho-on-base-set-aci-as-emissions-manager-for-rewards/19338)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x07784e062dd9c8cAB72a3479Ab6845aB77Ed162a)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x21eb25d3e2E2Cb45dBD5993a73bB95116944E147)

* Base - [proposal payloads](https://basescan.org/address/0x5F00667f40c6E4eD5B2a8Df7c3b4Ffac172B87cE)

* Base - gho listing - [proposal payloads](https://basescan.org/address/0xd359148d265ac7b85146393B074E89E74cAE2034)



## Certora Analysis

### Proposal Types
* :scroll: :small_red_triangle: Contract upgrades
* :handshake: Permission granting and revoking
* :gem: :new: Listing new assets

### Context
This AIP proposes the expansion of GHO, the native asset of the Aave Protocol, to the Base network utilizing the Chainlink Cross-Chain Interoperability Protocol (CCIP) v1.5.1.

The smart contracts have been refined through multiple stages of design, development, testing, and implementation. Likewise, Certora, the DAO service provider, was engaged to conduct code reviews of the implementation.


### Proposal Creation
Transaction: [0xdd7e7af051bd0bab63406c9952d493757dac68577a50b527af021b4f9956d540](https://etherscan.io/tx/0xdd7e7af051bd0bab63406c9952d493757dac68577a50b527af021b4f9956d540)
- `proposalId`: 240
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x77858639daf77d09480f14d12e25feb4bbea550c7f0187a7fd0503637425505b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 240,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 71,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 52,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 53,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x77858639daf77d09480f14d12e25feb4bbea550c7f0187a7fd0503637425505b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/240.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/240.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/71.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/52.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/53.md)


### Technical Analysis
We have reviewed the change thoroughly prior to the proposal, we ensured the upgrade is correctly implemented, the collector is funded prior to the listing and that CL proposed the governance as the new owners of the token pools.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 479. Orderly Transition and Offboarding Plan for Chaos Labs

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=479)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/orderly-transition-and-offboarding-plan-for-chaos-labs/24399)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4b481a81313dF60a9388a92c0ac058f41c8c08E8)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x64f7A73e90F0EcB08f629f361C0DfAB885A7642F)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x49d207360187cB0934CaF0f9A90e936ca60b7Cc5)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0xB5f598EE2379893CB64f1A6B8e27226Bf038c052)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x2517B88F3834bf39BEb1FEC059a91017dCf79502)

* Base - [proposal payloads](https://basescan.org/address/0x8a897be3D51d9B1679CF8E6FcF67212845af9C47)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x4EbA515691ea8a9EE6C224790b5015E776224990)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0x86C5ff084551FbFCfdf89E5f1171035667ea3383)

* Linea - [proposal payloads](https://lineascan.build/address/0xf8907160a29788A140b68775457A845b297979c6)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :bank: Payment stream

### Context
This proposal sets out a structured transition plan for Chaos Labs’ departure from its current role, with the objective of minimizing disruption to the DAO and maintaining continuity across key risk-management functions during the offboarding period.

In contrast to recent service provider departures, Aave has a secondary risk provider, which helps minimize the transition period and ensure a smooth continuation of operations.

As such, our intent is to complete this transition within 30 days. During that period, we will continue supporting the DAO in a clearly defined capacity, complete the handoff of ongoing responsibilities, and ensure that remaining operational dependencies are addressed in an orderly manner.

As part of this transition, Chaos Labs will cancel its outstanding stream and transfer the remaining stream funding corresponding to the 30-day transition period starting from the forum post date (April 8, 2026

### Proposal Creation
Transaction: [0xad96a0733cccc7cc0423908c9da539eb3a2f423f8231cd6e841108d4aa1637e5](https://etherscan.io/tx/0xad96a0733cccc7cc0423908c9da539eb3a2f423f8231cd6e841108d4aa1637e5)
- `proposalId`: 479
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xdeeeb58ec0c23fb201591b061fc2ff8d7964da844e352ff53d545b4271fd9d94

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 429,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 142,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 113,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 94,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 119,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 106,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 74,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 57,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 25,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xdeeeb58ec0c23fb201591b061fc2ff8d7964da844e352ff53d545b4271fd9d94",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/479.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/429.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/142.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/113.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/94.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/119.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/106.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/74.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/57.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/25.md)


### Technical Analysis

We have verified that the proposal revokes the Chaos Labs operational footprint across nine Aave V3 instances. On each L2 instance the payload removes the `RISK_ADMIN` role (`0x8aa855a911518ecfbe5bc3088c8f3dda7badf130faaf8ace33fdc33828e18167`) from the Chaos-Labs-controlled addresses on the corresponding `ACLManager`, disables their `AgentHub` agents, and cancels their `KeeperRegistry` / `AaveCLRobotOperator` upkeeps:

* Polygon - 2 `RISK_ADMIN` revocations (`0xd99D0A740AF7B68f1CB635294C013552423666b1`, `0xA512909edCf6D9aE46b0414ce0aD724968448177`), 2 agents disabled, 2 upkeeps cancelled.
* Avalanche - 3 `RISK_ADMIN` revocations (`0x38753B4D5116b12bC3524e334bC76AE57fA42fFB`, `0xb57C37F48d1De2DACBefed69679Ba0b7DC43A394`, `0x72b89100DB6f0Bde118Ebb34E71FA95A6DC59038`), 3 agents disabled, 3 upkeeps cancelled.
* Optimism - 2 `RISK_ADMIN` revocations (`0x8963Abfb008A668346B18d0BeE82b171F3b2Be24`, `0x3993695F48d64076C5Df1EeC9490501F9bB400C8`), 2 agents disabled, 2 upkeeps cancelled.
* Arbitrum - 3 `RISK_ADMIN` revocations (`0xeBe545478709d4388e36Bb706CF11e2f89898541`, `0x8963Abfb008A668346B18d0BeE82b171F3b2Be24`, `0xc42f40Bc50e7342867Be7F823a4358cba5089063`), 3 agents disabled, 3 upkeeps cancelled.
* Base - 3 `RISK_ADMIN` revocations (`0x42ca9E62C9B61d01Bb222d6E69f095eE98e61cE8`, `0x0ae2815b1f607EfEe34C15E63c72Cd6C99d1D6fa`, `0xAD83c71619368390c4C4fd1Aa472235FD4Ea3F32`), 3 agents disabled, 3 upkeeps cancelled.
* Gnosis - 2 `RISK_ADMIN` revocations (`0x8d3C192BC8D0913Ecc4eAACf0Fe99B6F6226B486`, `0xcCeb5996cF9976168fdbE6fF88B1d89e1180A0EA`), 2 agents disabled.
* BNB - 2 `RISK_ADMIN` revocations (`0x2cf0fA5b36F0f89a5EA18F835d1375974a7720B8`, `0x970dDfF6c38B29D67DFe282306f7c0e1f5f31207`), 2 agents disabled, 2 upkeeps cancelled.
* Linea - 1 `RISK_ADMIN` revocation (`0x58226D26658F19724cB881E9F747EeDC846BB1c9`), 1 agent disabled.

The Ethereum payload action contract (`0x4b481a81313dF60a9388a92c0ac058f41c8c08E8`) follows the same revocation pattern and additionally includes the cancellation of the Chaos Labs payment stream on the Aave Collector. Seatbelt simulation reverts for this payload; the mainnet stream-cancellation portion is completed in the follow-up proposals AIP-481 and AIP-485.

We have verified the payload's logic on each L2 and validated execution via Seatbelt for the eight L2 payloads.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 455. Activate Capo Risk Agent and expand Rates Agent on more networks

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=455)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-dynamic-calibration-of-capo-parameters-via-risk-oracles/22601)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xD163EDF944A652c3F7221962d6151D5f6ca59561)

* Ethereum 2 - [proposal payloads](https://etherscan.io/address/0x1A4FE4b74c7B649E5894b82b1eccD218BFe6914E)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x1A6f7855FfA29DA386119cf0EA9467b408EAd990)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x4c121FB6E65666F37d2c0a81cc42FaCC5a0a7220)

* Base - [proposal payloads](https://basescan.org/address/0x6b6486ff2413e76be1bfc2845054A599eD76c19f)

* Linea - [proposal payloads](https://lineascan.build/address/0xD534E6e80820732B44e296531eaa70e75444c675)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates


### Context
This proposal activates the new CAPO Risk Agent on Ethereum and expands the existing Slope2 Interest Rates Agent (live on Ethereum Core, Linea) to Avalanche, Arbitrum, and Base networks. Additionally, it aligns the Slope2 Interest Rates Agent constraints on Ethereum Core and Linea with the new networks.

### Proposal Creation
Transaction: [0xd590ef56833aa63e96ee94e43c5932c00ba090f66a9e318cb32e2bc163d2cf7e](https://etherscan.io/tx/0xd590ef56833aa63e96ee94e43c5932c00ba090f66a9e318cb32e2bc163d2cf7e)
- `proposalId`: 455
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xbf37418b8769c2526367ec784c39febe7480e0dfc87b361d5dd9ba8be56eb602

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 409,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 108,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 112,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 99,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 21,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xbf37418b8769c2526367ec784c39febe7480e0dfc87b361d5dd9ba8be56eb602",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/455.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/409.md)

* Ethereum 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/409.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/108.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/112.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/99.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/21.md)


### Technical Analysis

We confirmed the registration of the new risk agents on the AgentHub contract via the registerAgent() calls, alongside the correct initialization of the new Chainlink automation on the AgentHub Automation wrapper.

We verified that the `RangeValidationModule` is accurately configured enforcing a maximum 2% absolute change for stablecoins and 1.5% for WETH per 8 hours across the aligned Ethereum Core and Linea instances, as well as the newly expanded Avalanche, Arbitrum, and Base networks.

We confirmed the assignment of the `RISK_ADMIN` role to the AgentContract.

We verified that the reimbursement of 108 LINK to BGD Labs was executed via a withdrawal from the Aave Collector on Ethereum to cover previous out-of-pocket automation costs.

We have verified proposal logic and validate its execution via seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
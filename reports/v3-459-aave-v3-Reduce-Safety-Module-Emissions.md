# Proposal 459. Reduce Safety Module Emissions

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=459)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-safety-module-reduce-emissions/24203)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x17e15936a47Fe49644dA506f0EC76752CB93810e)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal reduces Safety Module emissions and adjusts parameters for stkAAVE and stkAAVE/wstETH BPTv2, saving a combined 29,200 AAVE/year (~0.18% of total supply, ~$3.6M) while transitioning stkAAVE/wstETH BPTv2 toward sunset in favour of Protocol-Owned Liquidity.

### Proposal Creation
Transaction: [0x89c00841d15de7ac9f6bf58c3e520d064bdf1a87c5d89eb63f3ebbde39a5e339](https://etherscan.io/tx/0x89c00841d15de7ac9f6bf58c3e520d064bdf1a87c5d89eb63f3ebbde39a5e339)
- `proposalId`: 459
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xd3906387c86728351e01c0017fee1b489ad4bd3e0f6dec26415b49fe86efb592

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 415,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xd3906387c86728351e01c0017fee1b489ad4bd3e0f6dec26415b49fe86efb592",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/459.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/415.md)


### Technical Analysis
The parameter configuration has been reviewed and verified to be correctly aligned with the intended changes.  
The payload execution flow was validated and confirmed to behave as expected, including successful verification using Seatbelt.  
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
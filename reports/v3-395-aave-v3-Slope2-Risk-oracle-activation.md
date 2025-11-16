# Proposal 395. Slope2 Risk Oracle Activation On Core Ethereum, Linea

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=395)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/118)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x92F7aC533aC1A88331EE24b77637788bfa257222)

* Linea - [proposal payloads](https://lineascan.build/address/0xe40BfEa9631788b19c38D6A51Ba3AF839d35C3ec)



## Certora Analysis

### Proposal Types


* :handshake: Permission granting and revoking


### Context
This proposal activates the automated Aave Generalized Risk Stewards (AGRS) system on the `Aave Ethereum Core` and `Linea` Instance to perform automated slope2 interest rate updates for WETH, USDT, USDC, USDe assets. Under the hood, the AGRS consumes the Risk Oracle infrastructure by Chaos Labs.

### Proposal Creation
Transaction: [0x811dff56d1dd8e3ee7976dd66faa4e1de40b1cc86518232cd275a15de8783a68](https://etherscan.io/tx/0x811dff56d1dd8e3ee7976dd66faa4e1de40b1cc86518232cd275a15de8783a68)
- `proposalId`: 395
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xd3bc49794f5a74d990ceeb6d30a88e3df1787ab9b8baf5db5c7b20f75051b515

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 362,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 14,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xd3bc49794f5a74d990ceeb6d30a88e3df1787ab9b8baf5db5c7b20f75051b515",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/395.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/362.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/14.md)


### Technical Analysis
We have confirmed alignment between the forum post, the IPFS content, and the on-chain payload.
We have validated the addresses of on both Linea and Ethereum `EDGE_RISK_STEWARD_RATES` and `EDGE_INJECTOR_RATES` on Ethereum. we confirmed payloads's logic and execution and reviewed the seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
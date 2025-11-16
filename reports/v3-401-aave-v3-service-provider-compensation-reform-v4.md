# Proposal 401. Service Provider Compensation Reform for V4 Alignment

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=401)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-service-provider-compensation-reform-for-v4-alignment/23246)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9bbd6164843AA0BB49954f32ccaE176ddd37b637)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers
* :wrench: :bar_chart: Configuration updates
* :bank: Payment stream

### Context
This AIP proposes a comprehensive reset of all active Aave service provider compensation streams to better align contributors with the success of the Aave ecosystem ahead of the Aave V4 launch.
The proposal maintains the same total annual compensation levels for each provider while introducing a one-year vesting component tied to clear key performance indicators (KPIs).

### Proposal Creation
Transaction: [0xdbcaffc871acb2f6bfb5a3621599b1d084f877004ed63d782ead8d1a1ade7c64](https://etherscan.io/tx/0xdbcaffc871acb2f6bfb5a3621599b1d084f877004ed63d782ead8d1a1ade7c64)
- `proposalId`: 401
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xadec1fb6812a8f5502d9011ecc87c484444ff615cdf00f38bc0f1cca036ab93b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 364,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xadec1fb6812a8f5502d9011ecc87c484444ff615cdf00f38bc0f1cca036ab93b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/401.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/364.md)


### Technical Analysis

We confirmed alignment between the forum post, IPFS, and the on-chain payload.
we have verified mentioned Assets addresses.
We have verified the service providers addresses in the `ReformData.sol` their specified amounts and stream durations / End.
We have validate the payload's logic and confirmed its execution via seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
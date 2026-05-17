# Proposal 485. Offboarding Plan for Chaos Labs part 3: Cancel stream 100073

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=485)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/orderly-transition-and-offboarding-plan-for-chaos-labs/24399)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3e0aFcA0aa407A7D322795C38B1575AB5c52Ba13)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates
* :bank: Payment stream

### Context
Follow-up payload to the orderly offboarding of Chaos Labs. This AIP cancels the outstanding payment stream 100073 on the Aave Prime collector. No other state is modified. The original offboarding payload (AIP-479) was unable to execute its mainnet portion in full, leaving stream 100073 active beyond the agreed offboarding window. Concurrently, the receiving address is no longer considered under Chaos Labs' operational control, and at Chaos Labs' request the offboarding is being completed via a direct stream cancellation rather than a continued transfer.

This AIP performs that single action so the offboarding can be closed out cleanly.

### Proposal Creation
Transaction: [0x9bf7f623cb3b397c53c77f5a98c467c0b2ef7417fb5d1b4beab85610e83297a0](https://etherscan.io/tx/0x9bf7f623cb3b397c53c77f5a98c467c0b2ef7417fb5d1b4beab85610e83297a0)
- `proposalId`: 485
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x50a8e9d7fae094f46526db2ef3593ca6217ac7b16601463d2a188e7b588b735b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 439,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x50a8e9d7fae094f46526db2ef3593ca6217ac7b16601463d2a188e7b588b735b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/485.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/439.md)


### Technical Analysis

We have verified that the payload performs a single action: cancellation of stream `100073` on the Aave Collector (`0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c`), matching the stream id referenced in the AIP description.

We have verified that the stream's storage is fully zeroed (deposit, rate per second, remaining balance, start/stop timestamps, recipient, sender and token address all reset), confirming a complete cancellation rather than a partial modification.

We have verified that the vested-but-unclaimed portion (~277,786.02 GHO) is transferred from the Collector to the stream recipient `0xbC540e0729B732fb14afA240aA5A047aE9ba7dF0` as part of the cancellation flow, and that no other Collector balances, role assignments, or stream entries are modified.

We have verified the payload's logic and validated its execution via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 268. Recreate wrstETH eMode on Base

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=268)

### Governance Forum Discussion
[Link to forum discussion](TODO)

### Payloads

* Base - [proposal payloads](https://basescan.org/address/0xD1A0BA620fF73aa327bC00A10eEc50E91DF70cE9)


## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Create a new eMode for wrsETH/wstETH and unfreeze wrsETH & LBTC. 

Just after listing, a misconfiguration involving the new eMode including wrsETH and another involving LBTC has been detected, with a race condition between two proposals running in parallel causing the rsETH eMode to have too conservative risk parameters but including on the same eMode both ETH assets (rsETH collateral, wstETH borrowable) and BTC assets (LBTC collateral, cbBTC borrowable).

Even if this doesn’t create any immediate risk to the protocol or these assets, this is a highly unexpected configuration, and we have recommended the Aave Protocol Guardian to freeze the assets affected (wrsETH and LBTC), as there were no user supplies yet.

A follow-up governance proposal will be submitted fixing the eMode configuration, and making both LBTC and wrsETH fully operative again.

### Proposal Creation
Transaction: [0x621b636e86c96bcb232cad8513dc75e2af155f67dbd77f5e9ef3fb1d508929e8](https://etherscan.io/tx/0x621b636e86c96bcb232cad8513dc75e2af155f67dbd77f5e9ef3fb1d508929e8)
- `proposalId`: 268
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xa04d3af3553db0dbc63ed3222f861663c121236b3ab279d8f75daba42bc0703b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 61,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xa04d3af3553db0dbc63ed3222f861663c121236b3ab279d8f75daba42bc0703b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/268.md)

**Payload Reports**

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/61.md)


### Technical Analysis
We have verified the new emode id is unique and only the intended asset are included with the correct risk parameters.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 346. Onboard USDe September expiry PT tokens on Aave V3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=346)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-usde-september-expiry-pt-tokens-on-aave-v3-core-instance/22620)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x51E6F2f47CD97B56AbdB3efb30E274Bbb7D5e2D3)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This AIP proposes to onboard USDe September expiry PT tokens on Aave V3 Core Instance.

### Proposal Creation
Transaction: [0xd9b5597dadddf1061c69b3af522963947acfaae91168fbd846d41147e5194d19](https://etherscan.io/tx/0xd9b5597dadddf1061c69b3af522963947acfaae91168fbd846d41147e5194d19)
- `proposalId`: 346
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xab453bc3008f4aa5fc0b04038d3ba4b274a5560bf24a16f6db01557006261fdf

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 321,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xab453bc3008f4aa5fc0b04038d3ba4b274a5560bf24a16f6db01557006261fdf",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/346.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/321.md)


### Technical Analysis
We have verified the address of the onboarded token. We have validated the correct assets were added to the emodes. We have confirmed the risk parameters were configured as specified.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 423. USDG Listing

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=423)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-usdg-to-aave-v3-core-instance/23271)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x92Cd4Fa690035752D49033335850005b3593640B)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets

### Context
We propose the onboarding of USDG, a USD-backed stablecoin issued by Paxos, on Aave V3 Core Instance. This listing would initially enable users to deposit USDG to earn yield and borrow USDG as a stable asset. Collateral usage will be considered at a later date following review by Aave's Risk Management teams. 
### Proposal Creation
Transaction: [0x2a19e4a63dc8a534ce6c7e6bd2c008c8363fec33396163024458d27da2c4d9be](https://etherscan.io/tx/0x2a19e4a63dc8a534ce6c7e6bd2c008c8363fec33396163024458d27da2c4d9be)
- `proposalId`: 423
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xa71c1ac091ede114488cebb1b8efce47b74217bbc15d25b89227c6fc249616f1

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 382,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xa71c1ac091ede114488cebb1b8efce47b74217bbc15d25b89227c6fc249616f1",
    access_level: 1,
}
```
### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/423.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/382.md)


### Technical Analysis
We have verified the imports.
We have verified alignment between the Forum, IPFS, and the payload risk parameters.
We have checked the seed supply amount with respect to decimal precision.
We have verified that all relevant addresses are correct, including the price feed and the emissions admin.
We have reviewed the payload’s execution logic and validated its execution via Seatbelt.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
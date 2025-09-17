# Proposal 364. Add XAUt to Aave v3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=364)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-add-xaut-to-aave-v3-core-instance/22385)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xD230e4605B231034909e1A838683cd9516BdA88B)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
The proposal aims to onboard Tether’s XAUt gold-denominated stablecoin, to the Aave v3 Core Instance.

### Proposal Creation
Transaction: [0x18e55bc3f88af95f90a35ed6db0e3776bbcdc27091990559a9eed876dfa722a5](https://etherscan.io/tx/0x18e55bc3f88af95f90a35ed6db0e3776bbcdc27091990559a9eed876dfa722a5)
- `proposalId`: 364
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xbb022e52cdf9d2b65b5e8cfd7a350fa7b3bc8149f80db0edbc7e52d1eb1b8a24

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 333,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xbb022e52cdf9d2b65b5e8cfd7a350fa7b3bc8149f80db0edbc7e52d1eb1b8a24",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/364.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/333.md)


### Technical Analysis
We have compared the risk parameters to forum and IPFS for inconsistencies. We have validated the seed amount. We have checked the price feed is correct.
 
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
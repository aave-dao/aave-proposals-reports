# Proposal 419. Alter mUSD Oracle Price Implementation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=419)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-alter-musd-oracle-price-implementation/23489)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x10fd96504c6470Ecc8CE56591827b36Ed1FE56dE)

* Linea - [proposal payloads](https://lineascan.build/address/0x3d6FD1e505CD4A69410f8133dB5534a90c626AeE)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
This proposal re-enables the supply and borrow caps for MetaMask USD (mUSD) on the Aave v3 Ethereum and Linea deployments while swapping the oracle feed on both networks to a static $1 adapter.

### Proposal Creation
Transaction: [0x1c5dbd6cd5da7770c56f56a1ce9ad9bcac1fd0dc49dd070b617d1448e4ab9467](https://etherscan.io/tx/0x1c5dbd6cd5da7770c56f56a1ce9ad9bcac1fd0dc49dd070b617d1448e4ab9467)
- `proposalId`: 419
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x322df3a160f7194d475d089dd25640806cc5b25c85a48c45f554bd002d51d34d

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 378,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 17,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x322df3a160f7194d475d089dd25640806cc5b25c85a48c45f554bd002d51d34d",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/419.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/378.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/17.md)


### Technical Analysis

We have verified consistency between the forum, IPFS, and the proposal payload. We have checked the integrity of the imports. We have reviewed the payload’s execution logic and validated it via Seatbelt. We have verified the new price feed addresses and confirmed that the answer is a constant $1. We have also checked the supply and borrow cap parameters and verified the token address. The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
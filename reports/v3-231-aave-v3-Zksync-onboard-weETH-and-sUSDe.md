# Proposal 231. Onboard sUSDe and weETH to Aave v3 on zkSync

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=231)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-susde-usde-and-weeth-to-aave-v3-on-zksync/19204)

### Payloads

* zkSync Era - [proposal payloads](https://era.zksync.network/address/0xa449606c98F0FBC98415C39Ccf373C1e5271f967)



## Certora Analysis

### Proposal Types
* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets

### Context
Following the original plans to further expend on the zkSync network, onboarding of 2 popular assets.

### Proposal Creation
Transaction: [0x0a4434b48ef8226bce022743d725a131654e7454ee9773905c52c0845ec47b41](https://etherscan.io/tx/0x0a4434b48ef8226bce022743d725a131654e7454ee9773905c52c0845ec47b41)
- `proposalId`: 231
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xe56f37dd9f78eaa77a7ac58af9ff61966c543a97c44a89160573629396aceceb

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 10,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xe56f37dd9f78eaa77a7ac58af9ff61966c543a97c44a89160573629396aceceb",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/231.md)

**Payload Reports**

* zkSync Era - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/10.md)


### Technical Analysis

The payload lists 2 new assets to the network - weETH and sUSDe with the specified parameters on the IPFS. In addition, it creates a weETH-WETH emode with the specified parameters and sets weETH as collateral only and WETH as borrow asset only.
On top of that, a reward emission admin is set to the specified address on both assets.

The proposal is consistent with the latest description on the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 389. Adopt The SEAL Safe Harbor Agreement

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=389)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-adopt-the-seal-safe-harbor-agreement/23059)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xBBfa2490332F93e33693dEE1933D2D5Ae8b64D80)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking

### Context
This proposal registers Aave's adoption of the SEAL (Security Alliance) Whitehat Safe Harbor Agreement on-chain. The agreement enables whitehats to legally intervene during active exploits to protect protocol funds, with clear rules for fund recovery, predefined bounties, and legal protections for good-faith actors.

### Proposal Creation
Transaction: [0xdc87aa2cb75867106132066e329a87f413e66776a748233b1f9816e160b83668](https://etherscan.io/tx/0xdc87aa2cb75867106132066e329a87f413e66776a748233b1f9816e160b83668)
- `proposalId`: 389
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xd610f641b1273ce491e1ec810059062fcd5776548358d921c51c67b25b1fd1f4

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 358,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xd610f641b1273ce491e1ec810059062fcd5776548358d921c51c67b25b1fd1f4",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/389.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/358.md)


### Technical Analysis
We can confirm this proposal does not create any state changes to the AAVE protocol. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
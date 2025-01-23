# Proposal 235. Set REZ, KERNEL and rsETH Emission Admin to ACI

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=235)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-set-rez-kernel-and-rseth-emission-admin-to-aci/20599)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x302FC2F8E4f52A711074Ca05E26D89a86F6b6DB5)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking

### Context
This proposal enables ACI to distribute REZ, KERNEL and rsETH rewards across several instances of Aave v3.

### Proposal Creation
Transaction: [0xee7b08008724981ff846542928f02180ffa56eabde257dd8db7e9be15a68afdf](https://etherscan.io/tx/0xee7b08008724981ff846542928f02180ffa56eabde257dd8db7e9be15a68afdf)
- `proposalId`: 235
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x9049e32e552aa49a718e0cd0b8a876f6d601919e978fd6c77848217f62dca5f6

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 236,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x9049e32e552aa49a718e0cd0b8a876f6d601919e978fd6c77848217f62dca5f6",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/235.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/236.md)


### Technical Analysis
We have verified the addresses of the tokens and the new emission admin multisig. we have also verified the the emission admin has been configured correctly.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
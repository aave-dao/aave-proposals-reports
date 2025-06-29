# Proposal 326. GHO Avalanche Launch

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=326)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-launch-gho-on-avalanche-set-aci-as-emissions-manager-for-rewards/19339)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xfC418D8e4d7FEEf9eE156A6b20c459D3A56097CC)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x8F0Ab79B3e4977ef932976d677D7d56C6C786a4e)

* Base - [proposal payloads](https://basescan.org/address/0xe5C4A212e9968F77980B7CDA4Bef3e33D4Eba086)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xee765B849270EA5dE708Db72b55A9023a00b5bFd)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xEd8b9765c22039E43512B8CA6263C90400965f6d)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This AIP proposes the expansion of GHO, the native asset of the Aave Protocol, to the Avalanche network utilizing the Chainlink Cross-Chain Interoperability Protocol (CCIP).

The smart contracts have been refined through multiple stages of design, development, testing, and implementation. Likewise, Certora, the DAO service provider, was engaged to conduct code reviews of the implementation.

### Proposal Creation
Transaction: [0xdcde1faf40d96076001d9e5573e9dbf98f81263119e8268ac3ba9a0f09969579](https://etherscan.io/tx/0xdcde1faf40d96076001d9e5573e9dbf98f81263119e8268ac3ba9a0f09969579)
- `proposalId`: 326
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x5a4f5b10da82c74af4f943b13f296ac2959dfede5eb42d01d23e6fb0e9158ca2

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 304,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 91,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 74,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 82,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 83,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x5a4f5b10da82c74af4f943b13f296ac2959dfede5eb42d01d23e6fb0e9158ca2",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/326.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/304.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/91.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/74.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/82.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/83.md)


### Technical Analysis
We have verified the risk parameters are correct and the bridge is setup correctly.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
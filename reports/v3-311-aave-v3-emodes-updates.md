# Proposal 311. LRT and wstETH Unification

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=311)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-lrt-and-wsteth-unification/21739)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xaEfd3D70312C121Baa40DC0153272aF5ABb07932)

* Ethereum 2 - [proposal payloads](https://etherscan.io/address/0x27fFdFe264f269CC6d40fe0B31b7313e976a462e)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x03dea926Dc6323db3965D02E01a47969319Db137)

* Base - [proposal payloads](https://basescan.org/address/0xB3c491aa77A015697007032015Ef110fFB6E3A2A)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This publication presents a comprehensive overview of proposed LRT and LST risk parameters updates across Ethereum, Prime, Base and Arbitrum instances of Aave v3.

### Proposal Creation
Transaction: [0xa164689bc928a0b6679cd60306bc6ab0fd1d1cbb18ea7fa30719684b35f8c7db](https://etherscan.io/tx/0xa164689bc928a0b6679cd60306bc6ab0fd1d1cbb18ea7fa30719684b35f8c7db)
- `proposalId`: 311
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x14eb1427fd0569fe42cbc068c05e5d01593d956a5e74184b278de555865dabc3

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 288,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 87,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 69,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x14eb1427fd0569fe42cbc068c05e5d01593d956a5e74184b278de555865dabc3",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/311.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/288.md)

* Ethereum 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/288.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/87.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/69.md)


### Technical Analysis
We have made sure the new emodes are in non occupied ID's. We have compared the values in the IPFS to the implementation with respect to scailing.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
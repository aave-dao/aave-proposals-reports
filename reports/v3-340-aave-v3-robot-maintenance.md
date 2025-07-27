# Proposal 340. Robot Maintenance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=340)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/96)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x80EaE07078858fc3f15d04ff5Aa21A7951b12057)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x5f10E166f6F4341F0AD1Fe0B4a4E9bB2FcF149B9)

* Polygon 2 - [proposal payloads](https://polygonscan.com/address/0xA76b883e198A3D143bF1a7504FBb2838203C6A54)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x2e9F8fF2B52931C88AE76196816Afa3A8f486953)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x95Fe7Abc19D7381470cB762177dC97Ec457458A0)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x8B5fC288abE20AE8BfdAcc081d552501EC4AC946)

* Base - [proposal payloads](https://basescan.org/address/0x9ED2E3D4da4652e58C6574e36a16C46444ECE37F)

* Base 2 - [proposal payloads](https://basescan.org/address/0xcF9B1fA683a30AE143F8bAFB099dBD9bBf2ADb76)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0xFC4224652BC029dcaDF8F912e55C99c0BCa641E6)

* BNB Smart Chain 2 - [proposal payloads](https://bscscan.com/address/0x3fD890e27A6A2a0bFD0D24919dafD07cb3ea213A)



## Certora Analysis

### Proposal Types
* :scroll: :small_red_triangle: Contract upgrades


### Context
Maintenance proposal to update the Aave Robot automations related with governance voting machines and Stata Tokens rewards accounting.

### Proposal Creation
Transaction: [0x4d47a5c8bc30815df796c10e1e5d09fb43f2a08306aa76a70974dea2f90670f4](https://etherscan.io/tx/0x4d47a5c8bc30815df796c10e1e5d09fb43f2a08306aa76a70974dea2f90670f4)
- `proposalId`: 340
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xd6840c447d1b8e455e7fe70d188d497cd1f4de37dfe6535d4720f9723cad0977

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 314,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 119,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 121,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 88,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 81,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 95,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 78,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 80,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 44,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 46,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xd6840c447d1b8e455e7fe70d188d497cd1f4de37dfe6535d4720f9723cad0977",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/340.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/314.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/119.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/88.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/81.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/95.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/78.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/44.md)


### Technical Analysis
We have verified and compared the addresses of the new `StataRefreshRewardRobot` and `VotingChainRobot`. We have checked the correctness of the proposal logic.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
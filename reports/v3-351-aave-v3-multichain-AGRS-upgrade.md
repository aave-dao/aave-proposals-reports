# Proposal 351. Caps Risk Oracle Activation on Optimism, BNB, Gnosis, Polygon

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=351)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/98)

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0xF78A1Abbd01e1CEBaF28467D151C64417b935bba)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0xa3D433f81019321458e3870932bC1A1B9075154f)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xa235ac66371488B6d7ee15833E7cbd6786A93baB)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0xCF93D6B1AE58c9C3fB4d4659B506668A62dC8473)



## Certora Analysis

### Proposal Types
* :scroll: :small_red_triangle: Contract upgrades

* :handshake: Permission granting and revoking

### Context
{**TODO: Write context.**}

### Proposal Creation
Transaction: [0xe428b481caa52d7044e712a10aba982ce8f23fd89f9a612cb73fe7c36761bbc4](https://etherscan.io/tx/0xe428b481caa52d7044e712a10aba982ce8f23fd89f9a612cb73fe7c36761bbc4)
- `proposalId`: 351
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xdd7635ee3afea99731d9a8b630170cdbaaf669103fbcb3e15a3da2603c955966

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 124,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 84,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 57,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 48,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xdd7635ee3afea99731d9a8b630170cdbaaf669103fbcb3e15a3da2603c955966",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/351.md)

**Payload Reports**

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/124.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/84.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/57.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/48.md)


### Technical Analysis
We have verified the addresses of all the components of the `AGRS`. We checked that the allowed tokens from the IPFS match the allowed markets in `AaveStewardCapsInjector` contract. We have confirmed the procedure and the LINK transfer in the payload have been done correctly.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
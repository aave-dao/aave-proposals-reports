# Proposal 491. stkAAVE Emissions Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=491)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-stkaave-emissions-update/24945)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xe3a0aa89fb826489d67bE0893072D8f578EF6E5F)



## Certora Analysis

### Proposal Types
* :wrench: :bar_chart: Configuration updates
* :bank: Payment stream

### Context
Reduce stkAAVE emissions from 220 AAVE/day to 150 AAVE/day, targeting a staking APR of ~2.75% (down from ~3.30%).

### Proposal Creation
Transaction: [0x093787f8abf96ff7070a85c71cd9db1d716ad326ab33cddd8309bcf91f399b60](https://etherscan.io/tx/0x093787f8abf96ff7070a85c71cd9db1d716ad326ab33cddd8309bcf91f399b60)
- `proposalId`: 491
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0xa2887b9f02ec3ec7e4eefbd74fc931537d51fd8d5e6412f1269ad2b209347218

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 445,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xa2887b9f02ec3ec7e4eefbd74fc931537d51fd8d5e6412f1269ad2b209347218",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/491.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/445.md)


### Technical Analysis

* We have verified that the payload's logic matches the AIP specification: it calls `IStakeToken(STK_AAVE).configureAssets()` with a single `AssetConfigInput` setting `emissionPerSecond` to `uint128(uint256(150 ether) / 1 days)` = `1,736,111,111,111,111` wei/s on stkAAVE (`0x4da27a545c0c5B758a6BA100e3a049001de870f5`).
* We have verified the math: 150 AAVE/day = `150e18 / 86400` = `1,736,111,111,111,111` wei/s, down from the previous rate of `2,546,296,296,296,296` wei/s (≈ 220 AAVE/day), confirming a reduction of ~31.9%.
* We have verified against the seatbelt state diff that `assets[stkAAVE].emissionPerSecond` changes from `2,546,296,296,296,296` to `1,736,111,111,111,111`, and that the `AssetConfigUpdated(asset: stkAAVE, emission: 1,736,111,111,111,111)` event is emitted as expected.
* We have verified that no allowance or token transfer actions are included — the payload only updates the emission rate and does not modify any existing distribution end timestamp or AAVE allowance on the Ecosystem Reserve.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
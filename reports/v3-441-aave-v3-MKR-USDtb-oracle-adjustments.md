# Proposal 441. MKR and USDtb oracle adjustments

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=441)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-mkr-and-usdtb-oracle-adjustments/23911)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x198854284D7fbBd6fE5E47B63432dd9B676CcF25)



## Certora Analysis

### Proposal Types


* :wrench: :bar_chart: Configuration updates


### Context
Proposal to, on Aave v3 Ethereum Core, replace the price feed of MKR with one calculated from SKY/USD Chainlink and the MKR-to-SKY migration contract, and USDtb by one statically pegged to 1 USD.

### Proposal Creation
Transaction: [0xc3b1483e54e4cb19609023db3017f678bdf56541b6b5eb87e73ce3c61fc29f8b](https://etherscan.io/tx/0xc3b1483e54e4cb19609023db3017f678bdf56541b6b5eb87e73ce3c61fc29f8b)
- `proposalId`: 441
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x1f7d3d7e913674118ae445add980901d70da9828a7316457db043d51d58da0cd

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 398,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x1f7d3d7e913674118ae445add980901d70da9828a7316457db043d51d58da0cd",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/441.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/398.md)


### Technical Analysis

We have verified that the new oracle addresses match the corresponding tokens.  
We have checked that the `DISCOUNT_PROVIDER` is the `MkrSky` migration contract.
We have also checked the proposal logic and verified its execution simulation using Seatbelt.  
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
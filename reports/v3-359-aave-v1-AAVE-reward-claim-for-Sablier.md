# Proposal 359. Claiming AAVE Rewards for the Sablier Legacy v1.1 Contract

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=359)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-claiming-aave-rewards-for-the-sablier-legacy-v1-1-contract/21975)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x98E5f4e669AbDC52C632CaB40aa17ce6aA76aC17)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers

### Context
This AIP proposes the transfer of **895.8057 AAVE** (~$160K) in staking rewards from the Aave Safety Module to **[sablier.eth](https://etherscan.io/address/0x5cE95bff1297dADBDcF9929a10Bd02BDfab0DCC6)**, due to the inability of Sablier’s Legacy v1.1 contract to claim them through standard mechanisms.


### Proposal Creation
Transaction: [0x00adf4cf2b25806fe39b39813c98994f06876873a2c6299dea04880e1ab94b70](https://etherscan.io/tx/0x00adf4cf2b25806fe39b39813c98994f06876873a2c6299dea04880e1ab94b70)
- `proposalId`: 359
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x5c6bcd27cc94e27f40112647e0fde323c17706ce82746008ceae9d707deb0208

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 330,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x5c6bcd27cc94e27f40112647e0fde323c17706ce82746008ceae9d707deb0208",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/359.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/330.md)


### Technical Analysis
We have validated the address and the general logic of the proposal is correct.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
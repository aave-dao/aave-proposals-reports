# Proposal 462. Aave V4 Activation on Ethereum Mainnet

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=462)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-v4-activation-on-ethereum-mainnet/24293)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9074eBd12E4d27458EE6000F70507ab2997ed903)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades
* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates


### Context
This AIP proposes the activation of Aave V4 on Ethereum Mainnet, through a security-first initial setup with conservative risk parameters and a deliberately narrow Hub and Spoke configuration.

### Proposal Creation
Transaction: [0x35745e9d7b5e73171b1d6ab63c5f7d575e77218474831dff7e9a94980148f04e](https://etherscan.io/tx/0x35745e9d7b5e73171b1d6ab63c5f7d575e77218474831dff7e9a94980148f04e)
- `proposalId`: 462
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x2befcdd0c2981dbc1d901e3117968bf56a8d5ed1c1a270a0b354094f36d02ea4

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 420,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x2befcdd0c2981dbc1d901e3117968bf56a8d5ed1c1a270a0b354094f36d02ea4",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/462.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/420.md)


### Technical Analysis
We confirmed the activation of the new risk Spokes on the `HubInstance` contracts via the `updateSpokeActive()` calls.

We verified that the Hubs are accurately configured to enforce the new risk isolation parameters for 17 assets on the Core Hub, 7 on the Plus Hub, and 7 on the Prime Hub, aligning the network with the V4 specifications.

We confirmed the assignment of the unlimited deposit capacity to the `Treasury Spoke` contract across all Hubs.

We have verified proposal logic and validate its execution via seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 475. April Funding Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=475)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-april-2026-funding-update/24447)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xEf6Ae1757E92b5B93515bA5fEec84634cCd616D3)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x968E08C9BB579A82fF40c7bbE0D3D14B636eee7D)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xafEba386582bA16f857E43C4FA7B9F93cf84C6d4)

* Base - [proposal payloads](https://basescan.org/address/0x9a9c58807E147a81fd5f59Ced5E105221632Ac4A)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x53A796702e66818C71619AC842F343d92704c39f)

* Linea - [proposal payloads](https://lineascan.build/address/0x1c5bC2D4F1A41FB2B1e5c66491a7F8a32bB2422A)

* Plasma - [proposal payloads](https://plasmascan.to/address/0xba1cd7e8fcd4e26d96ae01ede35d18464a5aaecb)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :bank: Payment stream

### Context
{**TODO: Write context.**}

### Proposal Creation
Transaction: [0xdbf378ecfb129261f51bff1062835e1af62e2e579f718abfd65e85ffb6028f3a](https://etherscan.io/tx/0xdbf378ecfb129261f51bff1062835e1af62e2e579f718abfd65e85ffb6028f3a)
- `proposalId`: 475
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0xb2375739f9140980dbafd68c7f7e2d0b71cd11de08ca2f0f8923aa9051b0202c

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 428,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 112,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 118,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 105,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 52,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 24,
        },
        {
            chain: "9745",
            payloads_controller: "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d",
            payload_id: 24,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xb2375739f9140980dbafd68c7f7e2d0b71cd11de08ca2f0f8923aa9051b0202c",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/475.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/428.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/112.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/118.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/105.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/52.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/24.md)

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/24.md)


### Technical Analysis

We have validated payloads and verified its execution via seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
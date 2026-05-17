# Proposal 473. Upgrade Aave instances to v3.7 Part 1

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=473)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-bgd-aave-v3-7/24075)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x924bd84976c144D291312ba2625d3a2d110DCC50)

* Ethereum 2 - [proposal payloads](https://etherscan.io/address/0x5132977cb38d22dc871afB99FF50c1DEfd8D9792)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0xAC9De98211625AA7420CC240b5c0635D7130F504)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x112590f08Ee593cE9486C3dEa834Bc833446F2Db)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xdC856109C36dc0310E46bEA9F661d39Df3b8badF)

* Celo - [proposal payloads](https://celo.blockscout.com/address/0xB3cF4b51Fee1CC092A2fE5fb98E392463dBD5f29)

* Sonic - [proposal payloads](https://sonicscan.org/address/0x3340417a17FcA7245C20B64EB001FA9c522A2EeE)

* MegaETH - [proposal payloads](https://mega.etherscan.io/address/0xff2dbfd40a7ccc1f9db952e6ed1f672554c16b25)

* Xlayer - [proposal payloads](https://www.oklink.com/xlayer/address/0x3f52906fb38cbd7ebe5ec0318170895dafdc7143)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades
* :wrench: :bar_chart: Configuration updates


### Context
Upgrade the Aave protocol instances from v3.6 to v3.7.

Aave v3.7 focused on non-invasive simplification of the protocol. It includes the following changes and features:

Simplification of eModes’ configuration, adding an isolated flag.
Removal of isolated collaterals and borrowable in isolation, features not useful anymore.
Removal of the L2 sequencer oracle.
Explicit removal of the flow to drop reserves, making the reserves list append-only.
Small improvements on liquidation calculations.


### Proposal Creation
Transaction: [0xcadf71017caaa018b356e2560eb6f509b865d40d770063ef64fdb6651eb703e1](https://etherscan.io/tx/0xcadf71017caaa018b356e2560eb6f509b865d40d770063ef64fdb6651eb703e1)
- `proposalId`: 473
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x812add4b4fcad057bac049fec938d5b5187be0ace246a7e336e5640e7a9c73d6

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 424,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 93,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 73,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 50,
        },
        {
            chain: "42220",
            payloads_controller: "0xE48E10834C04E394A04BF22a565D063D40b9FA42",
            payload_id: 11,
        },
        {
            chain: "146",
            payloads_controller: "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695",
            payload_id: 13,
        },
        {
            chain: "4326",
            payloads_controller: "0x80e11cB895a23C901a990239E5534054C66476B5",
            payload_id: 1,
        },
        {
            chain: "196",
            payloads_controller: "0x80e11cB895a23C901a990239E5534054C66476B5",
            payload_id: 3,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x812add4b4fcad057bac049fec938d5b5187be0ace246a7e336e5640e7a9c73d6",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/473.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/424.md)

* Ethereum 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/424.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/93.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/73.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/50.md)

* Celo - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42220/0xE48E10834C04E394A04BF22a565D063D40b9FA42/11.md)

* Sonic - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/146/0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695/13.md)

* MegaETH - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/4326/0x80e11cB895a23C901a990239E5534054C66476B5/1.md)

* Xlayer - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/196/0x80e11cB895a23C901a990239E5534054C66476B5/3.md)


### Technical Analysis

* **Transfers Verified:** Seatbelt reports confirm the exact decimal-precise transfers of aUSDT to BGD Labs and GHO to Certora on Ethereum Mainnet.

* **Constructors Verified:** All `POOL_ADDRESSES_PROVIDER` values correctly match `IPool(params.poolImpl).ADDRESSES_PROVIDER()`, ensuring safe deployments across all chains.

* **Pools Validated:** The provided target proxies match the official `AToken` and `VToken` pools.

* **Logic & Execution:** Payload logic and execution are verified. Pre-upgrade state cleanups (isolation flags, debt ceilings, oracles) executed correctly. Storage layout compatibility between implementations is validated.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
# Proposal 489. Upgrade Aave instances to v3.7 Part 2

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=489)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-bgd-aave-v3-7/24075)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x81b384AAc4fcCD95b5f7c4d4af5EFD3C11547Afe)

* Ethereum 2 - [proposal payloads](https://etherscan.io/address/0x225183208bdD562158b862f57f4536EcA231E724)

* Ethereum 3 - [proposal payloads](https://etherscan.io/address/0x045709CCA177d3550cA1FE610ec89D48E0A78d8C)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xCE327f36564c3D54b042AeF64A780E120e01383E)

* Polygon 2 - [proposal payloads](https://polygonscan.com/address/0xEEE8dFB21cE9b3576B09B572eEfE49dcD6BDf513)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x345128FbA0f7AEa020B4765C0bC3d6e8E212552A)

* Avalanche 2 - [proposal payloads](https://snowtrace.io/address/0x3af437799c7A6D49E15fb85a1F88567505680248)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x4C77AaC15Ca7C92d4638859f43Ee953AdCd8C351)

* Arbitrum One 2 - [proposal payloads](https://arbiscan.io/address/0x0B194DE42C3819bB0B681D3a432bFC03ae2AbF45)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0xB7b07787129AFb39F2d199dCae2AF838B55Cf566)

* Base - [proposal payloads](https://basescan.org/address/0xfA033Ba5A23F08c8C4cb577C8F6f119fB3bfB959)

* Base 2 - [proposal payloads](https://basescan.org/address/0xB6db55371B5Ae04C99e2C040c3cc012895C68e01)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0x55A4E6cd2Aa0ADDFE403a2Ae3B1522d3198b430E)

* BNB Smart Chain 2 - [proposal payloads](https://bscscan.com/address/0x1dA9a00D2D086080Dca17B10E29E6d34BbB8f15F)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xFE5a5455157EeE08b23dD3944863eFd5ca087606)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x8ebCd3e40A43DDfB106A7a035dD14B743E214f96)

* Linea - [proposal payloads](https://lineascan.build/address/0xD2cFB7Da9feC4e465674720e38Db7f3E04C40E7d)

* Linea 2 - [proposal payloads](https://lineascan.build/address/0xc817F2079BC78269d773c8BF55f1437A1917DD65)

* Sonic - [proposal payloads](https://sonicscan.org/address/0xf02f365893D5A68dD508323E1e899C0e78A4E781)

* Celo - [proposal payloads](https://celo.blockscout.com/address/0xE85E4bA6d8a7756d9652058B2dabf6B9e5ef527b)

* Plasma - [proposal payloads](https://plasmascan.to/address/0xde44e9a591e864cfa8b9fc762d5a7657771e1737)

* Plasma 2 - [proposal payloads](https://plasmascan.to/address/0xa69ce012643280099ec884274693c8eefecf3e5b)

* Mantle - [proposal payloads](https://mantlescan.xyz/address/0x79bAFd2535C7Dadd4e03F04B10c8F79553A03c3a)

* Mantle 2 - [proposal payloads](https://mantlescan.xyz/address/0xA7c395982E75F77BBbc7c54f20aa29b59ed58B90)

* MegaETH - [proposal payloads](https://mega.etherscan.io/address/0xf421ce2656c01c32ee96af40a20dda4e555d4778)

* Xlayer - [proposal payloads](https://www.oklink.com/xlayer/address/0x8b7ab53078a855497c940594afa2a877d97b1dcb)



## Certora Analysis

### Proposal Types
* :scroll: :small_red_triangle: Contract upgrades
* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates

### Context
Upgrade the Aave protocol instances from v3.6 to v3.7, and replaces the current RiskSteward with a newly deployed steward compatible with v3.7.

Aave v3.7 focused on non-invasive simplification of the protocol. It includes the following changes and features:
* Simplification of eModes’ configuration, adding an isolated flag.
* Removal of isolated collaterals and borrowable in isolation, features not useful anymore.
* Removal of the L2 sequencer oracle.
* Explicit removal of the flow to drop reserves, making the reserves list append-only.
* Small improvements on liquidation calculations.

### Proposal Creation
Transaction: [0xe9105ad53cdeed4589c6a3cb1c24480a9840626c9b009ba84c355eaff904aa8c](https://etherscan.io/tx/0xe9105ad53cdeed4589c6a3cb1c24480a9840626c9b009ba84c355eaff904aa8c)
- `proposalId`: 489
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x1771282791a2769a488791be8160020ac408bc74fa67ca7f107cab87a730b240

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 442,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 145,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 116,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 129,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 95,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 109,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 59,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 53,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 77,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 29,
        },
        {
            chain: "146",
            payloads_controller: "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695",
            payload_id: 14,
        },
        {
            chain: "42220",
            payloads_controller: "0xE48E10834C04E394A04BF22a565D063D40b9FA42",
            payload_id: 12,
        },
        {
            chain: "9745",
            payloads_controller: "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d",
            payload_id: 28,
        },
        {
            chain: "5000",
            payloads_controller: "0xF089f77173A3009A98c45f49D547BF714A7B1e01",
            payload_id: 7,
        },
        {
            chain: "4326",
            payloads_controller: "0x80e11cB895a23C901a990239E5534054C66476B5",
            payload_id: 7,
        },
        {
            chain: "196",
            payloads_controller: "0x80e11cB895a23C901a990239E5534054C66476B5",
            payload_id: 4,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x1771282791a2769a488791be8160020ac408bc74fa67ca7f107cab87a730b240",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/489.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/442.md)

* Ethereum 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/442.md)

* Ethereum 3 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/442.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/145.md)

* Polygon 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/145.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/116.md)

* Avalanche 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/116.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/129.md)

* Arbitrum One 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/129.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/95.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/109.md)

* Base 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/109.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/59.md)

* BNB Smart Chain 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/59.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/53.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/77.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/29.md)

* Linea 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/29.md)

* Sonic - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/146/0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695/14.md)

* Celo - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42220/0xE48E10834C04E394A04BF22a565D063D40b9FA42/12.md)

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/28.md)

* Plasma 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/28.md)

* Mantle - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/5000/0xF089f77173A3009A98c45f49D547BF714A7B1e01/7.md)

* Mantle 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/5000/0xF089f77173A3009A98c45f49D547BF714A7B1e01/7.md)

* MegaETH - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/4326/0x80e11cB895a23C901a990239E5534054C66476B5/7.md)

* Xlayer - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/196/0x80e11cB895a23C901a990239E5534054C66476B5/4.md)


### Technical Analysis

* **Constructors Verified:** All `POOL`, `POOL_ADDRESS_PROVIDER` and `POOL_CONFIGURATOR` values correctly match the addresses in the Aave adress book for the relevant chain and pool, ensuring safe deployments across all chains.

* **Pool Implementations Validated:** The provided new `POOL_IMPL` and `POOL_CONFIGURATOR_IMP` addresses, for each pool in each chain, where validated onchain as holding pool or pool configurator contracts.

* **RiskSteward Replacement:** We have verified that the new v3.7-compatible `RiskSteward` addresses are correctly deployed across all affected instances, and that the replaced `RiskSteward`s where correct. We confirmed that the `RISK_ADMIN` role is granted to the new steward and revoked from the prior steward on each chain.

* **RiskSteward GHO restrictions:** We have verified that for any `RiskSteward` change where GHO was not restricted, GHO is not listed in the pool's reserve list.

* **Logic & Execution:** Payload logic and execution are verified via Seatbelt. Pre-upgrade state cleanups (isolation flags, debt ceilings, oracles) executed correctly. Storage layout compatibility between implementations is validated.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
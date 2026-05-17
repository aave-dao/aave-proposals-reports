# Proposal 482. rsETH Incident: WETH LTV Restoration Across V3 Instances

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=482)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-weth-unfreeze-and-ltv-restoration-across-aave-v3-instances/24878)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3dC4836f6294C5E55A4B33563D0A172227054Ca6)

* Ethereum 2 - [proposal payloads](https://etherscan.io/address/0x38c58Aa751ee72Db0eBdE97094b63f74DFC45E3e)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x558818B0E36C1B061759D368EF6D75CbA10d0657)

* Base - [proposal payloads](https://basescan.org/address/0x3A64ce40Db785BF4381fBAb7cE767f9bb54DBD9A)

* Linea - [proposal payloads](https://lineascan.build/address/0x6E902b6287A3701A980C0b794F22794a2667617a)

* Mantle - [proposal payloads](https://mantlescan.xyz/address/0x3a3eC29d1434854f5525bECa55895066FC8317d5)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
Restore WETH Loan-to-Value (LTV) on Aave V3 Ethereum Core, Ethereum Prime, Arbitrum, Base, Mantle, Linea to their respective pre-exploit values. The Risk Guardian has already lifted the WETH freeze on the L2 instances where it remains in place. Together, these actions return the WETH market to normal operation across all Aave V3 deployments affected by the precautionary measures applied during the 2026-04-18 Kelp/LayerZero OFT bridge exploit.

### Proposal Creation
Transaction: [0xbb96aef34bf049c24bc850dbbba079b5d016406c3a24b7e2435d2cd9f66cbe89](https://etherscan.io/tx/0xbb96aef34bf049c24bc850dbbba079b5d016406c3a24b7e2435d2cd9f66cbe89)
- `proposalId`: 482
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x16ec0bfb8043ea427e92575a25036fcfba6f8581e236a0efaca1813ef1d32ff2

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 437,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 128,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 108,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 27,
        },
        {
            chain: "5000",
            payloads_controller: "0xF089f77173A3009A98c45f49D547BF714A7B1e01",
            payload_id: 5,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x16ec0bfb8043ea427e92575a25036fcfba6f8581e236a0efaca1813ef1d32ff2",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/482.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/437.md)

* Ethereum 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/437.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/128.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/108.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/27.md)

* Mantle - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/5000/0xF089f77173A3009A98c45f49D547BF714A7B1e01/5.md)


### Technical Analysis

We have verified that the proposal restores WETH collateral parameters across the targeted V3 instances, reversing the 0% LTV imposed during the rsETH incident response. Per the on-chain state-diff for each payload:

* Aave V3 Ethereum Core (WETH `0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2`): LTV `0% → 80.50%`, LT `0% → 83.00%`, LB unchanged at `5.00%`; WETH is unfrozen and removed from the eMode-1 zero-LTV bitmap.

* Aave V3 Ethereum Lido instance (same WETH address): LTV `0% → 84.00%`, LT `0% → 85.00%`, LB unchanged at `5.00%`; WETH is unfrozen.

* Aave V3 Arbitrum (WETH `0x82aF49447D8a07e3bd95BD0d56f35241523fBab1`): LTV `0% → 80.00%`, LT set to `84.00%`, LB at `5.00%`; WETH removed from the eMode-2 zero-LTV bitmap.

* Aave V3 Base (WETH `0x4200000000000000000000000000000000000006`): LTV `0% → 80.00%`; LT and LB retained at `83.00%` / `5.00%`; WETH removed from the eMode-1 zero-LTV bitmap.

* Aave V3 Linea (WETH `0xe5D7C2a44FfDDf6b295A15c148167daaAf5Cf34f`): LTV `0% → 80.00%`, LT `0% → 83.00%`, LB `6.00%`; the pending-LTV slot is cleared.

* Aave V3 Mantle (WETH `0xdeaddeaddeaddeaddeaddeaddeaddead1111`): LTV `0% → 80.50%`, LT `83.00%`, LB `5.50%`.

We have verified the payload's logic and validated its execution via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
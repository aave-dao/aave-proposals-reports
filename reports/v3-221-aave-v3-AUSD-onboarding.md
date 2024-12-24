# Proposal 221. Onboard AUSD

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=221)

### Governance Forum Discussions
[Link to forum discussions](https://governance.aave.com/t/arfc-onboard-ausd-to-aave-v3-on-avalanche/19689)

### Payloads

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x39FA6a2BC5Ca93fa2508C02202eC265F50Ed0c36)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets

### Context
This proposal seeks to onboard AUSD, a secure digital dollar backed 1:1 by USD fiat, to Aave V3 on Avalanche. AUSD, issued by Agora, serves as a stable and liquid alternative to USDT and USDC. With a growing AUM and robust liquidity, AUSD will enhance Aave’s liquidity pool, offering users a reliable and efficient stablecoin option with strong institutional backing.

### Proposal Creation
Transaction: [0xcaa1c6d32d0be15ce01522829122112cd65083d3708ac6cf24ea441bc88868ee](https://etherscan.io/tx/0xcaa1c6d32d0be15ce01522829122112cd65083d3708ac6cf24ea441bc88868ee)
- `proposalId`: 221
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x1d9a4b0e68334ee6c1f867d2bddc9eeafce96702d24f3a4280abbeb4c21164e3

**`createProposal()` Parameters**
```
{
    "payloads": [
        {
            "chain": "43114",
            "accessLevel": 1,
            "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            "payloadId": 63
        }
    ],
    "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    "ipfsHash": "0x1d9a4b0e68334ee6c1f867d2bddc9eeafce96702d24f3a4280abbeb4c21164e3"
}
```

### Aave Seatbelt Report
**Proposal Report**
[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/221.md)

**Payload Reports**

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/63.md)


### Technical Analysis
A comprehensive review was conducted to verify the proposed AUSD listing on Aave V3 against the provided documentation and governance resources. Below are the key findings:

- **Parameter Consistency**: The proposed risk parameters for AUSD were cross-checked with the details on IPFS and the Aave governance forum. All parameters are accurate and consistent across sources.
- **Token Address Verification**: The token address for AUSD is correctly provided as `0x00000000eFE302BEAA2b3e6e1b18d08D69a9012a`. This address matches the details specified in the proposal and associated documentation.
- **Emission Admin Configuration**: The emission admin for AUSD and the corresponding aToken has been accurately set to `0xac140648435d03f784879cd789130F22Ef588Fcd`. This was verified against the on-chain contract and governance discussions.
- **Risk Framework Alignment**: The listing parameters align with the Aave V3 framework, ensuring compliance with established standards for new asset onboarding.
- **Oracle Configuration**: The oracle address provided (`0x83f32c0882B12Ef16214c417efF11FD9e764bf34`) is valid and matches the governance proposal.

All components of the proposal have been validated for accuracy, and no discrepancies were identified. This ensures the integration of AUSD adheres to Aave's rigorous standards for asset onboarding.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
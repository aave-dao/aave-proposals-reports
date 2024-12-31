# Proposal 219. Aave Liquidity Committee Funding Phase V

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=219)

### Governance Forum Discussions
[Link to forum discussions](https://governance.aave.com/t/arfc-aave-liquidity-committee-funding-phase-v/20043)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xec89aED62B364816e965D27f658163B8877d7D34)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers

### Context
This proposal presents the Aave Liquidity Committee (ALC) Phase V request. Phase V focuses on reinforcing GHO’s peg stability and enhancing liquidity to enable seamless large swaps with minimal price impact. It also involves GHO's growth by expanding GHO to new networks, such as Base and Avalanche. New integrations aim to drive adoption by partnering with protocols such as Synthetix on Arbitrum, Fluid, and Gearbox on Mainnet. Additionally, innovative liquidity incentives, like Royco Quests, will further enhance user engagement and ecosystem participation. 

### Proposal Creation
Transaction: [0x524d1898ab6fd6b5d179fb9058d9d890eaf793b1c0c8d0410f39622132cb0241](https://etherscan.io/tx/0x524d1898ab6fd6b5d179fb9058d9d890eaf793b1c0c8d0410f39622132cb0241)
- `proposalId`: 219
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xa32fdf133e89c51329b6a20c66ab591b9c5f0e45176a21624834e4c0773bee17

**`createProposal()` Parameters**
```
{
    "payloads": [
        {
            "chain": "1",
            "accessLevel": 1,
            "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            "payloadId": 222
        }
    ],
    "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    "ipfsHash": "0xa32fdf133e89c51329b6a20c66ab591b9c5f0e45176a21624834e4c0773bee17"
}
```

### Aave Seatbelt Report
**Proposal Report**
[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/219.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/222.md)


### Technical Analysis
The technical analysis confirms the validity of the contract’s implementation. The addresses for the price feeders (MILKMAN) and oracles have been verified as accurate, ensuring proper functionality during swaps. Decimals and amounts for USDT, USDC, and GHO are correctly configured, aligning with their respective ERC-20 specifications. The swapping flow is thoroughly validated, ensuring that assets are properly withdrawn, swapped, and deposited without errors. Additionally, the contract resets allowances to zero before setting new values, adhering to ERC-20 standards and avoiding potential approval vulnerabilities.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
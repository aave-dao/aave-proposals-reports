# Proposal 386. Steward Deployment: MainnetSwapSteward and RewardsSteward

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=386)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-steward-deployment-mainnetswapsteward-and-rewardssteward/23070)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x79DdDe2FCF994A40c464c432696fA765F0eE0aDF)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xb9bD7F5337083e09A86d316dfc7Ad98487AF7E09)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xC75a2318e55326AFA9089F6fAFd19BC7Fb7Fa6Ee)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x646450F5BdFD5C53E4B38B48c7e4bD6F73032534)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xeD377764129f28210EdA0ECfdDD00ff49E8A2941)

* Base - [proposal payloads](https://basescan.org/address/0x89B13F8Ca0Ce89DedaF4Ec62Ce1a1459b0497eD4)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x1D211eBA90c105aA4191C3910B49f805980D8571)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xE3b2E6B18A6E2D56fdA619296b7Ef752c872fC5f)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0x3B9Cf1F8dAAdffE0E3B5C25B3bD2992e5AfFF995)

* Sonic - [proposal payloads](https://sonicscan.org/address/0xc4fb5F1842D1f9b7221bcd605Ebfc60BF8160DE1)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking


### Context
Expanding the Aave Finance Steward role to perform swaps on Ethereum via MainnetSwapSteward v1 and claim Liquidity Mining rewards across accrued to the collector across all networks via the RewardsSteward. Activating these steward roles will enable Aave DAO to further streamline operations and reduce governance overhead in a secure and safe manner.

### Proposal Creation
Transaction: [0x1a77dd05b485fdaef5d696cf444487ff8472f61ee85e6dc24648c56dd64fcd1c](https://etherscan.io/tx/0x1a77dd05b485fdaef5d696cf444487ff8472f61ee85e6dc24648c56dd64fcd1c)
- `proposalId`: 386
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x12336adc222eebaab850aeb03af054fc513611c0045aa5034acb38b214bdd94b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 354,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 130,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 98,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 86,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 104,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 87,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 63,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 47,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 49,
        },
        {
            chain: "146",
            payloads_controller: "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695",
            payload_id: 10,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x12336adc222eebaab850aeb03af054fc513611c0045aa5034acb38b214bdd94b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/386.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/354.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/130.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/98.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/86.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/104.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/87.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/63.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/47.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/49.md)

* Sonic - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/146/0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695/10.md)


### Technical Analysis
We have verified the budget of each token, we have confirmed the permission procedure is correct. We have checked each payload logic to call the correct address for the correct instance in the network. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
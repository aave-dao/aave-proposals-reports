# Proposal 154. Aave v3 Ethereum - listing of LUSD

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=154](https://app.aave.com/governance/proposal/?proposalId=154)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-add-lusd-to-ethereum-v3-market/11522](https://governance.aave.com/t/arc-add-lusd-to-ethereum-v3-market/11522)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists LUSD (LUSD Stablecoin, Liquity) on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xca9e8cb07c47d66858d91b71cb4d86a6eb8c64271c70c4da158cee2c461dbef1](https://etherscan.io/tx/0xca9e8cb07c47d66858d91b71cb4d86a6eb8c64271c70c4da158cee2c461dbef1)

```
- id: 154
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9d4948be10dce66c0f584a6c42fd7d985786b439]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16641699
- endBlock: 16660899
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x2544be91c00601ccaf3824eaa990c4ba92b2c2652f21713de2c7d46eb8c848be
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/154.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/154.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x9D4948Be10dcE66C0F584A6C42Fd7d985786b439#code) follows the new approach for listings, using the [Aave V3 listing engine contract](https://etherscan.io/address/0xC51e6E38d406F98049622Ca54a6096a23826B426#code), containing logic to expose a simple interface for listings, and do proper validations.

We have verified this payload respects the interface required by the v3 listing engine and effectively configures the LUSD listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 4%
  - Variable borrow slope 2: 87%
  - Optimal point: 80%
- The asset is not enabled as collateral
- Reserve Factor: 10%
- Liquidation protocol fee: 10%
- Supply cap: 3'000'000 LUSD
- Borrow cap: 1'210'000 LUSD
- No eMode category
- No isolation mode
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is the [Chainlink LUSD/USD feed](https://etherscan.io/address/0x3D7aE7E594f2f2091Ad8798313450130d0Aba3a0#code).

The initial configuration is completely aligned with the description on the Aave governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

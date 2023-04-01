# Proposal 190. Aave v3 Ethereum, Arbitrum - update of supply caps

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=190](https://app.aave.com/governance/proposal/?proposalId=190)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-gauntlet-recommendations-for-aave-link-and-weth-on-v3-arbitrum-2023-03-21/12394](https://governance.aave.com/t/arc-gauntlet-recommendations-for-aave-link-and-weth-on-v3-arbitrum-2023-03-21/12394)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates supply caps on Aave v3 Ethereum and Arbitrum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4cd3456f92f028f20fb45eb4b7e2141472d474654ae77fc11f558f3e2cdc236a](https://etherscan.io/tx/0x4cd3456f92f028f20fb45eb4b7e2141472d474654ae77fc11f558f3e2cdc236a)

```
- id: 190
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x142dcaec322aaa25141b2597bf348487adbd596d,0x2e2b1f112c4d79a9d22464f0d345de9b792705f1]
- values: [0,0]
- signatures: [execute(),execute(address)]
- calldatas: [0x,0x0000000000000000000000004c68fda91bfb4683eab90017d9b76a99f2d77eed]
- withDelegatecalls: [true,true]
- startBlock: 16929484
- endBlock: 16948684
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe95cda38231468aed501ed1d748b41f19a7888350fa5384cecf2dc76f8285351
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/190.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/190.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Arbitrum on the non-Ethereum interaction.
The proposals payloads do the following:

**[Ethereum](https://etherscan.io/address/0x142DCAEC322aAA25141B2597bf348487aDBd596d#code#F21#L1)**

This payload is correctly created with the new [BGD's Aave Config Engine of Aave v3 Ethereum](https://etherscan.io/address/0xE202F2fc4b6A37Ba53cfD15bE42a762A645FCA07#code#F18#L1) as target, doing the following changes:

- rETH supply cap: 10'000 rETH -> **20'000 rETH**
- CRV supply cap: 62'500'000 CRV -> **51'000'000 CRV**

<br>

**[Arbitrum](https://arbiscan.io/address/0x4c68fda91bfb4683eab90017d9b76a99f2d77eed#code#F21#L1)**

This payload is also correctly created with the new [BGD's Aave Config Engine of Aave v3 Arbitrum](https://arbiscan.io/address/0x0efdfc1a940de4e7e6acc9bb801481f81b17fd20#code#F18#L1) as target, doing the following changes:

- WETH supply cap: 35'280 WETH -> **45'000 WETH**


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

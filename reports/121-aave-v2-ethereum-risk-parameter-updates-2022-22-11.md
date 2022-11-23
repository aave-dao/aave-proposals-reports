# Proposal 121. Aave v2 Ethereum - Risk Parameter Updates 2022-22-11

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=121](https://app.aave.com/governance/proposal/?proposalId=121)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-recommendations-for-aave-v2-eth-2022-11-22/10757](https://governance.aave.com/t/arc-risk-parameter-recommendations-for-aave-v2-eth-2022-11-22/10757)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:ice_cube: freeze-asset

<br>

### Context

This proposal is an update of risk parameters on Aave v2 Ethereum by Gauntlet, to freeze multiple assets, given the current situation of volatility in the market.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8a03e955415009e1e1af771cb5cbc7298e23af249f0d3af36a2d1cba120814c0](https://etherscan.io/tx/0x8a03e955415009e1e1af771cb5cbc7298e23af249f0d3af36a2d1cba120814c0)

```
- id: 121
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0]
- signatures: [,,,,,,,,,,,,,,,,]
- calldatas: [0x7aca76eb0000000000000000000000000bc529c00c6401aef6d220be8c6ea1667f6ad93e,0x7aca76eb000000000000000000000000d533a949740bb3306d119cc777fa900ba034cd52,0x7aca76eb000000000000000000000000e41d2489571d322189246dafa5ebde1f4699f498,0x7aca76eb0000000000000000000000000f5d2fb29fb7d3cfee444a200298f468908cc942,0x7aca76eb000000000000000000000000111111111117dc0aa78b770fa6a738034120c302,0x7aca76eb0000000000000000000000000d8775f648430679a709e98d2b0cb6250d2887ef,0x7aca76eb00000000000000000000000057ab1ec28d129707052df4df418d58a2d46d5f51,0x7aca76eb000000000000000000000000f629cbd94d3791c9250152bd8dfbdf380e2a3b9c,0x7aca76eb000000000000000000000000056fd409e1d7a124bd7017459dfea2f387b6d5cd,0x7aca76eb000000000000000000000000d46ba6d942050d489dbd938a2c909a5d5039a161,0x7aca76eb00000000000000000000000003ab458634910aad20ef5f1c8ee96f1d6ac54919,0x7aca76eb0000000000000000000000008e870d67f660d95d5be530380d0ec0bd388289e1,0x7aca76eb0000000000000000000000005f98805a4e8be255a32880fdec7f6728c6568ba0,0x7aca76eb0000000000000000000000008798249c2e607446efb7ad49ec89dd1865ff4272,0x7aca76eb0000000000000000000000001494ca1f11d487c2bbe4543e90080aeba4ba3c2b,0x7aca76eb000000000000000000000000d5147bc8e386d91cc5dbe72099dac6c9b99276f5,0x7aca76eb0000000000000000000000009f8f72aa9304c8b593d555f12ef6589cc3a579a2]
- withDelegatecalls: [false,false,false,false,false,false,false,false,false,false,false,false,false,false,false,false,false]
- startBlock: 16035767
- endBlock: 16054967
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe26d1feceabefae6e63aa72c5aa30747387b847f6be3c605b39b645a4a1cd2f4
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/121.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/121.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the calldata submitted as payload of the proposal freezes multiple assets on Aave v2 Ethereum, by calling `freezeReserve()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code).
The affected assets are:
- YFI
- CRV
- ZRX,
- MANA
- 1INCH
- BAT
- sUSD
- ENJ
- GUSD
- AMPL
- RAI
- USDP
- LUSD
- xSUSHI
- DPI
- renFIL
- MKR

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.

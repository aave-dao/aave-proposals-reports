# Proposal 128. Aave v3 Polygon - addition of EMISSION_ADMINs for LDO, stMATIC, MaticX and SD

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=128](https://app.aave.com/governance/proposal/?proposalId=128)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-stmatic-maticx-emission-admin-for-polygon-v3-liquidity-pool/10632](https://governance.aave.com/t/arc-stmatic-maticx-emission-admin-for-polygon-v3-liquidity-pool/10632)

[https://governance.aave.com/t/arc-ldo-emission-admin-for-polygon-v3-liquidity-pool/10575](https://governance.aave.com/t/arc-ldo-emission-admin-for-polygon-v3-liquidity-pool/10575)

[https://governance.aave.com/t/arc-sd-emission-admin-for-polygon-v3-liquidity-pool/10658](https://governance.aave.com/t/arc-sd-emission-admin-for-polygon-v3-liquidity-pool/10658)

<br>

## BGD analysis

<br>

### Proposal types

:link: :bridge_at_night: cross-chain execution

:gift: rewards

<br>

### Context

This proposal sets EMISSION_ADMIN roles for different entities to configure rewards of LDO, stMATIC, MATICX and LDO, on Aave v3 Polygon.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x28c5e7419c7a91a596848c35b767edd5745b65d64af75d7627444bcf4565960a](https://etherscan.io/tx/0x28c5e7419c7a91a596848c35b767edd5745b65d64af75d7627444bcf4565960a)

```
- id: 128
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000007e8f833d23e19e88e3781ca913d674a2d5178fa1]
- withDelegatecalls: [true]
- startBlock: 16133133
- endBlock: 16152333
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x780a2b877ea3b13c924a30d2959ea0b8f0257799f1d4d743ed58f8783f529954
```

<br>

### Aave Seatbelt report

**Ethereum report:**
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/128.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/128.md)

**Polygon report:**
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/128_fx_8_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/128_fx_8_0.md)

<br>

### Technical analysis

From a technical point of view, we have verified that:
- The proposal uses properly cross-chain governance through the [Polygon's Cross-chain Forwarder](https://etherscan.io/address/0x158a6bc04f0828318821bae797f50b0a1299d45b#code) contract.
- The [payload on Polygon](https://polygonscan.com/address/0x7e8f833d23e19e88e3781ca913d674a2d5178fa1#code) correctly calls `setEmissionAdmin()` on the [Aave v3 Polygon Emission Manager contract](https://polygonscan.com/address/0x048f2228D7Bf6776f99aB50cB1b1eaB4D1d4cA73#code), on the 4 intended assets.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

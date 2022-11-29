# Proposal 125. Aave v2 Ethereum - Risk Parameter Updates 

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=125](https://app.aave.com/governance/proposal/?proposalId=125)

<br>

### Governance forum discussion

[https://governance.aave.com/t/risk-parameter-updates-for-aave-v2-ethereum-liquidity-pool-2022-11-25/10824](https://governance.aave.com/t/risk-parameter-updates-for-aave-v2-ethereum-liquidity-pool-2022-11-25/10824)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is an update of risk parameters on Aave v2 Ethereum by Chaos Labs and Llama, applying more granular changes than the ones on [proposal 121](https://app.aave.com/governance/proposal/?proposalId=121).


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x69c0b60d20fbf415f04a471d944d81f590a8dce3e21994248606ab1b0c995ebc](https://etherscan.io/tx/0x69c0b60d20fbf415f04a471d944d81f590a8dce3e21994248606ab1b0c995ebc)

```
- id: 125
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x53d3d14f9b2b8fe12d0da6864c76ed565716570e]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16055505
- endBlock: 16074705
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x401526716b075f2f211f4309ab895e7ada1c6e9e00c17ee13a4980776457ab21
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/125.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/125.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the proposal payload does the following changes on Aave v2 Ethereum, by interacting with the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code):

- YFI
  - **Freeze** (already frozen by 121, so no extra effect)

- CRV
  - **Unfreeze**
  - **Disable borrowing**

- ZRX
  - **Freeze** (already frozen by 121, so no extra effect)

- MANA
  - **Freeze** (already frozen by 121, so no extra effect)

- 1INCH
  - **Unfreeze**
  - **Disable borrowing**  

- BAT
  - **Freeze** (already frozen by 121, so no extra effect)

- sUSD
  - **Unfreeze**

- ENJ
  - **Freeze** (already frozen by 121, so no extra effect)

- GUSD
  - **Unfreeze**

- AMPL
  - **Freeze** (already frozen by 121, so no extra effect)

- RAI
  - **Freeze** (already frozen by 121, so no extra effect)

- USDP
  - **Unfreeze**

- LUSD
  - **Unfreeze**

- xSUSHI
  - **Freeze** (already frozen by 121, so no extra effect)

- DPI
  - **Unfreeze**

- renFIL
  - **Freeze** (already frozen by 121, so no extra effect)

- MKR
  - **Unfreeze**
  - **Disable borrowing**

- ENS
  - **Disable borrowing**

- LINK
  - **Disable borrowing** (already disabled by 122)

- UNI
  - **Disable borrowing** (already disabled by 123)

- SNX
  - **Disable borrowing**



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

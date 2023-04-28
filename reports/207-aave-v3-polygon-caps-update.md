# Proposal 207. Aave v3 Polygon - Caps update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=207](https://app.aave.com/governance/proposal/?proposalId=207)

<br>

### Governance forum discussion

[https://governance.aave.com/t/gauntlet-recommendations-for-eurs-on-v3-polygon/12798](https://governance.aave.com/t/gauntlet-recommendations-for-eurs-on-v3-polygon/12798)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the borrow cap of EURS on Aave v3 Polygon.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xf2668a14ee1f9ea1be9a1aba3caf3bad40338a6a2f6e55daa2e9dcd99b0fd99a](https://etherscan.io/tx/0xf2668a14ee1f9ea1be9a1aba3caf3bad40338a6a2f6e55daa2e9dcd99b0fd99a)

```
- id: 207
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000033deac0861fd6a9235b86172aa939e79085c6f52]
- withDelegatecalls: [true]
- startBlock: 17127012
- endBlock: 17146212
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x8e036cb7b5c10028564ba8d16c19e1b8bda48fa41edb904caec571908a76b1d3
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/207.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/207.md)


**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/207.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/207_fx_29_0.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

From a technical perspective, we have verified the [proposal payload](https://polygonscan.com/address/0x33deac0861fd6a9235b86172aa939e79085c6f52#code#F1#L1) correctly uses the new [BGD's Aave Config Engine of Aave v3 Polygon](https://polygonscan.com/address/0xE202F2fc4b6A37Ba53cfD15bE42a762A645FCA07#code#F18#L1), in this case, to update the following risk parameters the borrow cap of EURS from 947'000 EURS to **1'500'000 EURS**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

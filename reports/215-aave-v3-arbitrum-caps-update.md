# Proposal 215. Aave v3 Arbitrum - Caps update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=215](https://app.aave.com/governance/proposal/?proposalId=215)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-gauntlet-recommendations-for-polygon-v3-and-arbitrum-v3/12919](https://governance.aave.com/t/arc-gauntlet-recommendations-for-polygon-v3-and-arbitrum-v3/12919)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the supply and borrow caps of EURS on Aave v3 Arbitrum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa926884a75a45397eaa76a2fec7d798a1ab9654bb34ddd8b5d3a4f5d1b45f6ad](https://etherscan.io/tx/0xa926884a75a45397eaa76a2fec7d798a1ab9654bb34ddd8b5d3a4f5d1b45f6ad)

```
- id: 215
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000006bce15b789e537f3aba3c60cb183f0e8737f05ec]
- withDelegatecalls: [true]
- startBlock: 17190432
- endBlock: 17209632
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x5ef5fe9fcc8b8f5748b49dce1260e48e95065526f3a1b36752f068addc08715c
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/b83e74938fced0f827b0238dfeb15659bd5d04da/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/215.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/b83e74938fced0f827b0238dfeb15659bd5d04da/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/215.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Arbitrum.

From a technical perspective, we have verified the [proposal payload](https://arbiscan.io/address/0x6bce15b789e537f3aba3c60cb183f0e8737f05ec#code#F1#L1) correctly uses the new [BGD's Aave Config Engine of Aave v3 Arbitrum](https://arbiscan.io/address/0x0efdfc1a940de4e7e6acc9bb801481f81b17fd20#code#F18#L1), in this case, to update both the supply and borrow caps of EURS  the following way:
- Supply cap: 60'000 EURS -> **65'000 EURS**
- Borrow cap: 45'000 EURS -> **65'000 EURS**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

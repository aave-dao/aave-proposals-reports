# Proposal 135. Aave v3 Polygon - upgrade RewardsController of periphery to v3.0.1

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=135](https://app.aave.com/governance/proposal/?proposalId=135)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-upgrade-of-aave-v3-periphery-to-3-0-1-across-networks/10744](https://governance.aave.com/t/bgd-upgrade-of-aave-v3-periphery-to-3-0-1-across-networks/10744)

<br>

## BGD analysis

<br>

### Proposal types

:link: :bridge_at_night: cross-chain execution

<br>

### Context

This proposal upgrades the implementation of the RewardsController smart contract on Aave v3 Polygon, part of the denominated Aave periphery.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3ffee989323bee854db2187f8cd0be335e5ea04facdf3effa4e5fb4e9526bec5](https://etherscan.io/tx/0x3ffee989323bee854db2187f8cd0be335e5ea04facdf3effa4e5fb4e9526bec5)

```
- id: 135
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000f50a080ac535e531ec33cc05b227e910de2fb1fa]
- withDelegatecalls: [true]
- startBlock: 16234678
- endBlock: 16253878
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x277482762a64f4b0e666d5567d9f081465655ec9f26dc22d8cb9735784c5813e
```

<br>

### Aave Seatbelt report

**Ethereum report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/135.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/135.md)

**Polygon report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/135_fx_9_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/135_fx_9_0.md)

<br>

### Technical analysis

This proposal has been created by BGD Labs, so we find more appropriate to describe what exactly the [the proposal's payload](https://polygonscan.com/address/0xf50a080ac535e531ec33cc05b227e910de2fb1fa#code) does:
- First, it is important to clarify that this is a cross-chain proposal, so the target on Ethereum is the [CrosschainForwarderPolygon](https://etherscan.io/address/0x158a6bc04f0828318821bae797f50b0a1299d45b#code).
- The payload on Polygon upgrades the implementation of the RewardsController proxy, by calling `setAddressAsProxy()` on the [Aave V3 Polygon AddressesProvider contract](https://polygonscan.com/address/0xa97684ead0e402dc232d5a977953df7ecbab3cdb) with the id registered for the RewardsController (`keccak256("INCENTIVES_CONTROLLER")`) and the address of the [new implementation](https://polygonscan.com/address/0x5f4d15d761528c57a5c30c43c1dab26fc5452731#code).
- The revision of the new implementation is `2`, properly higher than the current version `1`.
- To avoid any attack surface, the implementation contract has been initialized too. 


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD wrote the payload.

:white_check_mark: With BGD writing the payload, at least another party reviewed it.
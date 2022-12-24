# Proposal 134. Aave v2 Ethereum - update renFIL interest rate strategy

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=134](https://app.aave.com/governance/proposal/?proposalId=134)

<br>

### Governance forum discussion

[https://governance.aave.com/t/update-renfil-interest-rate-strategy-on-aave-v2-ethereum/11049](https://governance.aave.com/t/update-renfil-interest-rate-strategy-on-aave-v2-ethereum/11049)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal minimizes the interest rate parameters of renFIL on Aave v2 Ethereum, by replacing its rate strategy contract.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x29c79a00f935948dfd3dff560212e6634fc20eb09e30c4904fb015333cd46935](https://etherscan.io/tx/0x29c79a00f935948dfd3dff560212e6634fc20eb09e30c4904fb015333cd46935)

```
- id: 134
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xbfcf7a2d4a91e91c72cdcf07ec65de6bf507daab]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16233437
- endBlock: 16252637
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x6e0d5a583e556e7bd8d1b9e3456b34ac085539320e248446792ea3600af12af0
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/134.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/134.md)

**There seems to be some infrastructure problem on Tenderly, which causes the state transitions to show erroneously (`aTokenAddress` instead of the correct `interestRateStrategyAddress`). We have double checked both payload code and events emitted, and everything seems correct**

<br>

### Technical analysis

This proposal has been created by BGD Labs, so we find more appropriate to describe what exactly the [the proposal's payload](https://etherscan.io/address/0xbfcf7a2d4a91e91c72cdcf07ec65de6bf507daab#code) does:
- The payload calls the [Pool Configurator of Aave v2 Ethereum](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756) to set as rate strategy of renFIL [THIS ONE](https://etherscan.io/address/0x311C866D55456e465e314A3E9830276B438A73f0#code).
- The new rate strategy return zero value for all external functions, which as explained on the [repository of this project](https://github.com/bgd-labs/aave-v2-zero-rate-strategy), doesn't cause any problem to the protocol.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD wrote the payload.

:white_check_mark: With BGD writing the payload, at least another party reviewed it.

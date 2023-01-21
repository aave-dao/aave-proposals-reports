# Proposal 144. Consolidation of Aave v3 Ethereum Collector's funds

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=144](https://app.aave.com/governance/proposal/?proposalId=144)

<br>

### Governance forum discussion
[https://governance.aave.com/t/arfc-ethereum-v2-collector-contract-consolidation/10909/15](https://governance.aave.com/t/arfc-ethereum-v2-collector-contract-consolidation/10909/15)

<br>

## BGD analysis

<br>

### Proposal types

:credit_card: funds-allowance

<br>

### Context
This proposal approves a set of smart contracts to proceed with a swap of multiple assets held by the v2 Collector to USDC.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0xc8fdc66d287d9fca1595afe22ac81d5e760d977ea28d8d232814c724f5e70868](https://etherscan.io/tx/0xc8fdc66d287d9fca1595afe22ac81d5e760d977ea28d8d232814c724f5e70868)

```
- id: 144
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xbefcd01681224555b74eac87207eaf9bc3361f59]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16442362
- endBlock: 16461562
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xdfb4dfe48453691fbeac9238f4954338ffa3ac10b56e77b63d3d1d76eae8b327
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/144.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/144.md)


<br>

### Technical analysis

This proposal, similar to previous ones introducing a swap mechanism, has 2 different layers: the payload contract and the actual system doing the swap.

**Proposal payload**
The [proposal payload](https://etherscan.io/address/0xbefcd01681224555b74eac87207eaf9bc3361f59#code) does the following:
1. Transfers to a [AMMWithdrawer contract](https://etherscan.io/address/0x334c59E5a50932a3C34AC39AB12131C648Cc1aE8#code) the aTokens from the AMM pool accrued on the Collector.
2. Triggers the `redeem()` function on the contract on 1).
3. Approves a [AaveV2CollectorContractConsolidation contract](https://etherscan.io/address/0xa426759e433224C2b04f6619aB44217DaD626c6e#code) to spend the current balance of aTokens from the v2 pool accrued on the Collector.

It is important to highlight that these balances are growing over time, so we think it is correct how the payload manages that, by using `balanceOf()` at the moment of payload's execution.

**AmmWithdrawer contract**

Simple contract that, assuming it has balance of aAMMDAI, aAMMUSDC, aAMMUSDT, aAMMWBTC and aAMMWETH, withdraws them (becoming DAI, USDC, USDT, WBTC and WETH) to the v2 Collector.
The contract is correct and functional, but being just 1 step, this operation could have been done on the proposal payload.

**AaveV2CollectorContractConsolidation contract**

This contract implements a mechanism to acquire USDC by selling a list of aTokens (e.g. aTUSD) and "underlyings" (e.g. TUSD) from the v2 Collector. This mechanism works as follows:
- The contract assumes to have certain allowance of all the tokens to be sold for USDC. Apart from that allowance, there is limit on how much to sell on each defined on construction of the smart contract.
- Anybody can call the `purchase()` function, passing the token and amount to buy. This will calculate the USDC required to receive that amount of tokens requested, transfer the USDC from the purcharser to the v2 Collector, and transfer the tokens from the Collector to the purchaser.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

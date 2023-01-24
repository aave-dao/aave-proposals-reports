# Proposal 146. Acquisition and repayment of CRV bad debt

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=146](https://app.aave.com/governance/proposal/?proposalId=146)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-repay-excess-crv-debt-on-ethereum-v2/10955](https://governance.aave.com/t/arfc-repay-excess-crv-debt-on-ethereum-v2/10955)

<br>

## BGD analysis

<br>

### Proposal types

:credit_card: funds-allowance

<br>

### Context

This proposal approves the swap of 3'105'000 aUSDC to CRV, in order to repay a maximum of 2'700'000 CRV, accrued as bad debt of Aave v3 Ethereum on address [https://etherscan.io/address/0x57E04786E231Af3343562C062E0d058F25daCE9E](https://etherscan.io/address/0x57E04786E231Af3343562C062E0d058F25daCE9E).

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x36baea71bd7c3c099aae8ff8d1035cb236dfc8e8eee42d9ad1592e3bc3ba4771](https://etherscan.io/tx/0x36baea71bd7c3c099aae8ff8d1035cb236dfc8e8eee42d9ad1592e3bc3ba4771)

```
- id: 146
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xaa7ef2f9b31fa26e802ca9b3e33990ada4143fb9]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16457332
- endBlock: 16476532
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x7c6a40470320bb6adb687cd9c5e8d73694c8af364579250a9d887031af4077ce
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/146.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/146.md)

<br>

### Technical analysis

This proposal, similar to previous ones introducing a swap mechanism, has 2 different layers: the payload contract and the actual system doing the swap.

**Proposal payload**

The [proposal payload](https://etherscan.io/address/0xaa7ef2f9b31fa26e802ca9b3e33990ada4143fb9#code) does the following:

- Gives allowance of 3'105'000 aUSDC from the Aave v2 Ethereum Collector to a helper smart contract [CRVBadDebtRepayment](https://etherscan.io/address/0x46A1B7d4a2920270c7eB2C2Db4DF2259A109bcb4#code), that will be used to acquire CRV. There is a typo in the comments referring to 2'000'000 aUSDC from a previous version, but the code is correctly operation over 3'105'000 aUSDC.
- Gives allowance of 2'700'000 CRV from the Aave v2 Ethereum Collector to the same CRVBadDebtRepayment, in order to, after the swap aUSDC->CRV happens, repay the bad debt of the defined address.

**CRVBadDebtRepayment**

Following same approach as other proposals like 115 or 144, this contract allows for purchasers to take an asset from the Collector (aUSDC) by delivering an amount of another asset (CRV) at a fair price determined by a Chainlink price feed.
In addition, it exposes a `repay()` function, that assuming allowance of CRV from the Aave v2 Collector (received previously from the proposal payload), allows for anybody to do a repayment on behalf of the account with bad debt.

Extra details and validations on the smart contract:

- The maximum repayment of CRV is limited to 2'700'000 CRV, the allowance given on the payload. No matter the holding of CRV in the Collector or timing of the swap, no extra debt will be repaid, unless CRVBadDebtRepayment receives extra allowance in the future.
- The maximum amount that can be ever be used of aUSDC is limited to 3'105'000 aUSDC, enforce too by the allowance given on the payload.
- `purchase()` respects CEI and it is reasonable, with the state updating before the release of the funds.
- Addresses of assets involved are correct, and amounts are consistent with the ones defined on the governance forum.
- Premium is consistent with the one defined on the forum: 10 bps.
- The `rescueTokens()` for an emergency scenario properly transfer always to the Aave v2 Collector.
- The purchaser can choose if receiving aUSDC or USDC, which doesn't present any problem.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

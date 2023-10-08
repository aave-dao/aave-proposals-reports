# Proposal 337. Aave v3 Optimism - enable OP as non-isolated collateral and borrowable

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=337](https://app.aave.com/governance/proposal/?proposalId=337)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-op-risk-parameters-update-aave-v3-optimism-pool/14633](https://governance.aave.com/t/arfc-op-risk-parameters-update-aave-v3-optimism-pool/14633)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal enables the OP asset as standard collateral on Aave v3 Optimism, removing it from isolation mode.

Additionally, OP is enabled as borrowable asset.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9c867de1325d5a9fa3c6f794c4d079dd30fe684f3b167db0a25b5ff51cd0a3ac](https://etherscan.io/tx/0x9c867de1325d5a9fa3c6f794c4d079dd30fe684f3b167db0a25b5ff51cd0a3ac)

```
- id: 337
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000e704efe305b14bddbba3d6c7f4a559149edc1339]
- withDelegatecalls: [true]
- startBlock: 18292478
- endBlock: 18311678
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xad4da707ea4fc4356bd22a0eba7a1bf824ec052f8e1579b2f939509751743f0d
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/337.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/337.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/337_Optimism_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/337_Optimism_pending_0.md)


<br>

### Technical analysis

The [proposal payload](https://optimistic.etherscan.io/address/0xe704efe305b14bddbba3d6c7f4a559149edc1339#code#F1#L13) correctly uses the BGD's Aave Config Engine of Aave v3 Optimism, in this case, for the following:

1. Remove OP from isolation mode, by setting its debt ceiling parameter to 0. The other current risk parameters are kept as previously configured.

2. Set a borrow cap of 500'000 OP.

3. Enabled OP as borrowing asset. The interest rate strategy is already configured from listing the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 7%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%

The payload is aligned with the description on the Aave governance forum and Snapshot.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

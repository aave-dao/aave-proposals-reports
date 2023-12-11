# Proposal 399. Aave v3 Ethereum - GHO variable debt token upgrade

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=399](https://app.aave.com/governance/proposal/?proposalId=399)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-technical-incident-13-11-2023/15642](https://governance.aave.com/t/arfc-gho-technical-incident-13-11-2023/15642)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :computer: contract-upgrade

<br>

### Context

This proposal upgrades the variable debt GHO implementation, fixing an issue reported via the Aave <> Immunefi program.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x03053a4f79ebea76708c7c7f504cfcf0f3e0c870ee3aad0645b48b9c15ea6507](https://etherscan.io/tx/0x03053a4f79ebea76708c7c7f504cfcf0f3e0c870ee3aad0645b48b9c15ea6507)

```
- id: 399
- creator: 0x8938be93f45c0da5d26894fe115d989149a90732
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000021]
- withDelegatecalls: [false]
- startBlock: 18744316
- endBlock: 18763516
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf4aa6f8da161b0c4bbc086bf0012fb29282e511226bc72c91e50ab58471a7044
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/399.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/399.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/33.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/33.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xbC9ffee8d18d75a412474B92192257d3c18471FF#code#F1#L14) properly upgrades the vGHO (variable debt GHO token) implementation with [this one](https://etherscan.io/address/0x20Cb2f303EDe313e2Cc44549Ad8653a5E8c0050e#code#F1#L29).

On the new implementation, we have reviewed the following:
- The `DEBT_TOKEN_REVISION` is correctly set to `3`, from the current `2` value.
- Even if this is part of the scope of Certora who reviewed the code, the change is pretty isolated and consistent with what high-level seems like a proper fix. For transparency, as reviewers on the Aave <> Immunefi program, we have visibility into the bug reported, and we helped reviewing its validity.
- Nothing else changes compared with the previous implementation.

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

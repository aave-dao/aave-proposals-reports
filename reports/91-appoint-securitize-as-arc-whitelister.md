# Proposal 91. Aave Arc - Appoint Securitize as Whitelister

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=91](https://app.aave.com/governance/proposal/?proposalId=91)

<br>

### Governance forum discussion
[https://governance.aave.com/t/arc-appoint-securitize-as-a-whitelister-to-aave-arc/6434](https://governance.aave.com/t/arc-appoint-securitize-as-a-whitelister-to-aave-arc/6434)

<br>

## BGD analysis

### Proposal types

:door: permissions

:shinto_shrine: Aave Arc

<br>

### Context
This proposal enables Securitize as permissions's admin on Aave Arc, allowing them to whitelist/blacklist users to participate on Arc.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0x1a31392fba51ae17f9f53f059d890b4812f7ea95a6a835e96c243f350475bd0c](https://etherscan.io/tx/0x1a31392fba51ae17f9f53f059d890b4812f7ea95a6a835e96c243f350475bd0c)
```
- id: 91
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xace1d11d836cb3f51ef658fd4d353ffb3c301218]
- values: [0]
- signatures: [queue(address[],uint256[],string[],bytes[],bool[])]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000e0000000000000000000000000000000000000000000000000000000000000012000000000000000000000000000000000000000000000000000000000000001a000000000000000000000000000000000000000000000000000000000000002600000000000000000000000000000000000000000000000000000000000000001000000000000000000000000f4a1f5fea79c3609514a417425971fadc10ecfbe0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000001e6164645065726d697373696f6e41646d696e7328616464726573735b5d2900000000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000100000000000000000000000036b8a1d23bdc76092ad88a1c4ef59fafd4931b0300000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000]
- withDelegatecalls: [false]
- startBlock: 15224040
- endBlock: 15243240
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xd0b98a12db1859322818b5943127735ca545d437d09dc0aa7dbcf9e66ac01569
```

<br>

### Aave Seatbelt report
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/091.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/091.md)

<br>

### Technical analysis
From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following on Aave Arc, by queueing an action on the [ArcTimelock contract](https://etherscan.io/address/0xAce1d11d836cb3F51Ef658FD4D353fFb3c301218):

1. Calls `addPermissionAdmins()` on the [Arc PermissionManager](https://etherscan.io/address/0xF4a1F5fEA79C3609514A417425971FadC10eCfBE#code) passing as parameter the new admin: an address belonging to Securitize, `0x36b8A1D23BDc76092aD88A1c4Ef59fafD4931b03`.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:x: BGD reviewed the payload before the proposal was submitted.
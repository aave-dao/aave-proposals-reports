# Proposal 106 (& complementary 107). Update of Aave Governance Level 2 requirements

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=106](https://app.aave.com/governance/proposal/?proposalId=106)

[https://app.aave.com/governance/proposal/?proposalId=107](https://app.aave.com/governance/proposal/?proposalId=107)

<br>

### Governance forum discussion

[https://governance.aave.com/t/rfc-aave-governance-adjust-level-2-requirements-long-executor/8693](https://governance.aave.com/t/rfc-aave-governance-adjust-level-2-requirements-long-executor/8693)

<br>

## BGD analysis

<br>

### Proposal types

:raising_hand: governance-changes

<br>

### Context

This proposals update the voting/proposing requirements of the Level 2 (most restrictive) part of the Aave Governance.
Proposal 106 executes the aforementioned updates, while 107 is a "vote boost" proposal, for the AAVE Ecosystem Reserve to vote YES on 106 with its AAVE holdings.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x7e46cc8d6b70be15d3e2948810eaf994c04192252a910a742f2d1f0e55458310](https://etherscan.io/tx/0x7e46cc8d6b70be15d3e2948810eaf994c04192252a910a742f2d1f0e55458310)


**Main proposal**

```
- id: 106
- creator: 0x6e1a6728829bc0fca82c1a39834c6212c250f1c1
- executor: 0x61910ecd7e8e942136ce7fe7943f956cea1cc2f7
- targets: [0x8e1b4169701a4acbf2936ec9e53fdbe8697f9703]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15696386
- endBlock: 15760386
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x4bd95ce6e9a0d76c0dd3154da423f01ee010ea9491bb5ddf5a151e6ef22b674c
```

**Vote boost proposal**

```
- id: 107
- creator: 0x6e1a6728829bc0fca82c1a39834c6212c250f1c1
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets:[0xb439ee42954da799bc835b7c9f117aea68c03f90]
- values": [0]
- signatures: [execute(uint256)]
- calldatas:[0x000000000000000000000000000000000000000000000000000000000000006a]
- withDelegatecalls:[true]
- startBlock: 15696386
- endBlock: 15715586
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x9c4249b03cdf9c2721b8b69d82a51bac19f35f4adbd09f194cc7d0cc449141d2
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/106.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/106.md)

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/107.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/107.md)

<br>

### Technical analysis

**Main proposal (106)**

From a technical perspective, the proposal:

- "Whitelists" on the AaveGovernanceV2 contract the [Executor with the updated governance requirements](https://etherscan.io/address/0x79426A1c24B2978D90d7A5070a46C65B07bC4299).
- Transfers the ownership of AaveGovernanceV2 to the new Executor.
- Transfers the proxy admin of AAVE and stkAAVE to the new Executor.
- Transfers the proxy admin of ABPT (AAVE/WETH Balancer Pool) and stkABPT to the Level 1 Executor, as they are not enabled as voting assets on the governance.

<br>

**Vote boost proposal**

This proposal only upgrades the implementation of the [AAVE Ecosystem Reserve](https://etherscan.io/address/0x25F2226B597E8F9514B3F68F00f494cF4f286491) to one with an `initialize()` function with the capability of voting once in an Aave governance proposal, in this case, proposal 106.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:white_check_mark: With BGD writing the payload, at least another party reviewed it.

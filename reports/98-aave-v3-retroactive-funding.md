# Proposal 98. Aave V3 retroactive funding to the Aave genesis team

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=98](https://app.aave.com/governance/proposal/?proposalId=98)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-aave-v3-retroactive-funding/9250](https://governance.aave.com/t/arc-aave-v3-retroactive-funding/9250)

<br>

## BGD analysis

<br>

### Proposal types

:money_with_wings: funds-release

:link: :bridge_at_night: cross-chain execution

<br>

### Context

This proposal releases funds of multiple assets from the collectors of Aave v2 Ethereum and Aave v2 Polygon to an account controlled by the Aave genesis team, as retro-active compensation for the development of Aave v3.

:exclamation: :exclamation: **IMPORTANT** During this analysis, we detected the Polygon side of the proposal will fail on execution if some permissions are not received on smart contracts of the Aave system before the execution time.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x25ca35f005aae409fc35bfc2be4edfc221d12fbb58ab47d0ad16f5aadb5ced85](https://etherscan.io/tx/0x25ca35f005aae409fc35bfc2be4edfc221d12fbb58ab47d0ad16f5aadb5ced85)

```
- id: 98
- creator: 0xdc6d052700a2bb1f45852a65acb61c194ef09b61
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xdb89487a449274478e984665b8692afc67459def,0xfe5e5d361b2ad62c541bab87c45a0b9b018389a2]
- values: [0,0]
- signatures: [execute(),sendMessageToChild(address,bytes)]
- calldatas: [0x,0x000000000000000000000000dc9a35b16db4e126cfedc41322b3a36454b1f7720000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000024000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000e00000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000018000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000001000000000000000000000000ccf14215e0134d6709c7dd7fa172cec40e97bfb100000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000004614619540000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001]
- withDelegatecalls: [true,false]
- startBlock: 15479095
- endBlock: 15498295
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x38f48494a97a61ec7500a8f8c92e4a233dd4bda22255a72ceb76d7025952bf69
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/098.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/098.md)


<br>

### Technical analysis

Even if simple in nature, the implementation of this proposal is extensive, and involving interaction with systems on Ethereum (collector of Aave v2 Ethereum), together with cross-chain interaction (Polygon), involving contract upgrades.
As commented previously, there is a mistake on the Polygon, but given the isolation of the Ethereum/Polygon actions, this would/will only make the Polygon actions fail on execution.

To simplify the analysis, we will split per network:

<br>

**Ethereum**

The Ethereum side of the proposal simply releases amounts of a set of pre-defined assets from the [Aave v2 Collector](https://etherscan.io/address/0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c) and the [AAVE ecosystem reserve](https://etherscan.io/address/0x25F2226B597E8F9514B3F68F00f494cF4f286491), to a Gnosis Safe defined as the recipient of the [Aave genesis team](https://etherscan.io/address/0x1c037b3C22240048807cC9d7111be5d455F640bd).

We have verified:
- The proper `transfer()` functions are called on the correct [controller of collector smart contract](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code).
- Both the v2 collector and the AAVE ecosystem reserves hold enough funds for the transfers.
- The assets transferred and amounts are as defined in the AIP text, but the sync between forum description, Snapshot and final aip is quite convoluted.

We can't verify assessments on the calculations of amounts involving prices (with discount), because it is not completely clear on the specifications.

In addition, the proposal doesn't establish any lock-up mechanism on AAVE/stkAAVE as defined on the forum, which we believe is really misleading, as it simply transfers AAVE to the Aave genesis team account.

<br>

**Polygon**

The second action of the proposal communicates with main component of the Polygon generic messaging bridge, the [FxRoot smart contract](https://etherscan.io/address/0xfe5e5d361b2ad62c541bab87c45a0b9b018389a2#code).

The messaged transfer to Polygon has as target the [PolygonBridgeExecutor](https://polygonscan.com/address/0xdc9A35B16DB4e126cFeDC41322b3a36454B1F772#code) on the Polygon network. On that side, a wrapper proposal will be queued to then execute the logic contained on the [PolygonProposalPayload](https://polygonscan.com/address/0xdc9A35B16DB4e126cFeDC41322b3a36454B1F772#code), which does the following:

- Tries to upgrade the implementations under transparent proxy of both the [v2 collector of Polygon](https://polygonscan.com/address/0x7734280A4337F37Fbf4651073Db7c28C80B339e9) and the [v3 collector](https://polygonscan.com/address/0xe8599F3cc5D38a9aD6F3684cd5CEa72f10Dbc383#code).
The new implementation used is the one deployed [HERE](https://polygonscan.com/address/0xC773bf5a987b29DdEAC77cf1D48a22a4Ce5B0577), which properly has `REVISION` 2. We have verified that this implementation has the functions to transfer and approve funds, but we would like to highlight that this is not the most updated version of the collector, as it lack streaming capabilities included into the one of Aave v2 Ethereum.
In addition, the implementation lacks the usage of `safeTransfer()` and `safeApprove()`, which should not affect at the current moment, but could create problems and require an extra upgrade down the line.
- The `_fundsAdmin` variable is assigned to a [CollectorController](https://polygonscan.com/address/0xDB89487A449274478e984665b8692AfC67459deF#code) smart contract, which has permissions over `approve()` and `transfer()` of the collector, and which in turn is controlled by the PolygonBridgeExecutor, executing the payload of this proposal.
- Both the v2 collector and the AAVE ecosystem reserves hold enough funds for the transfers.
- The assets transferred and amounts are as defined in the AIP text.

As we commented before, currently the PolygonBridgeExecutor executing the proposal doesn't have the `admin` role of the collector v2 transparent proxy, so the proposal will fail unless those permissions will be transferred before execution time. We have communicated the proposer the problem.

We highly encourage all parties contributing to Aave with proposals to, especially on relatively complex technical contributions like this one, ask a review in advance from BGD and follow standardise security procedures like the usage of this template repository for cross-chain proposal testing and creation [https://github.com/bgd-labs/aave-v3-crosschain-listing-template](https://github.com/bgd-labs/aave-v3-crosschain-listing-template).



<br>

### BGD validations

:x: Proposal fails partially on execution.

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets, with both CALL and DELEGATECALL

:white_check_mark: ** The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.


** The test suite doesn't detect the proposal failing, so it doesn't provide full proper coverage
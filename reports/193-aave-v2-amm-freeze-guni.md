# Proposal 193. Aave v2 Ethereum AMM - Freezing of G-UNI DAI/USDC and G-UNI USDC/USDT

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=193](https://app.aave.com/governance/proposal/?proposalId=193)

<br>

### Governance forum discussion

No forum discussion link for the proposal.

<br>

## BGD analysis

<br>

### Proposal types

:ice_cube: freeze-asset

<br>

### Context

The proposal freezes G-UNI DAI/USDC and G-UNI USDC/USDT on Aave v2 Ethereum, given the low liquidity levels of the reserves, which increase their risk profile.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6acd07cd53ed05f746869c72baff64d3a46cd8cec7f2849a38b891389f7c2484](https://etherscan.io/tx/0x6acd07cd53ed05f746869c72baff64d3a46cd8cec7f2849a38b891389f7c2484)

```
- id: 193
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x23a875ede3f1030138701683e42e9b16a7f87768,0x23a875ede3f1030138701683e42e9b16a7f87768]
- values: [0,0]
- signatures: [,]
- calldatas: [0x7aca76eb00000000000000000000000050379f632ca68d36e50cfbc8f78fe16bd1499d1e,0x7aca76eb000000000000000000000000d2eec91055f07fe24c9ccb25828ecfefd4be0c41]
- withDelegatecalls: [false,false]
- startBlock: 16943775
- endBlock: 16962975
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe30803793ff6ae0ad674cb9cda780af6183cf51c1757f807e37307069b3a6048
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/193.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/193.md)


<br>

### Technical analysis

The proposal payload (submitted via calldata) interacts with the [Aave v2 Ethereum AMM Pool Configurator](https://etherscan.io/address/0x23a875ede3f1030138701683e42e9b16a7f87768) to call the `freezeReserve()` function for both G-UNI DAI/USDC and G-UNI USDC-USDT.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the payload before the proposal was submitted.

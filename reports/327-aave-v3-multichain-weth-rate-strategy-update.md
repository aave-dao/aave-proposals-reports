# Proposal 327. Aave v3 Arbitrum, Optimism, Polygon, Metis - WETH interest rate update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=327](https://app.aave.com/governance/proposal/?proposalId=327)

<br>

### Governance forum discussion

[https://governance.aave.com/t/gauntlet-interest-rate-recommendations-for-weth-and-wmatic-on-v2-and-v3/14588/8](https://governance.aave.com/t/gauntlet-interest-rate-recommendations-for-weth-and-wmatic-on-v2-and-v3/14588/8)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategy of WETH on Aave v3 Polygon, Arbitrum, Optimism and Metis.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4e6cbe89a54708d6fc0cdbf250efe7ac50f81ae219a551a27d0c790cca4b2949](https://etherscan.io/tx/0x4e6cbe89a54708d6fc0cdbf250efe7ac50f81ae219a551a27d0c790cca4b2949)

```
- id: 327
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3,0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711,0x158a6bc04f0828318821bae797f50b0a1299d45b,0x2fe52ef191f0be1d98459bdad2f1d3160336c08f]
- values: [0,0,0,0]
- signatures: [execute(address),execute(address),execute(address),execute(address)]
- calldatas: [0x0000000000000000000000001cdb984008dcee9d06c28654ed31cf82680eea62,0x000000000000000000000000fc7b55cc7c5bd3ae89ac679c7250ab30754c5cc5,0x0000000000000000000000007aa759a57c6b039a93e93683facd14209ee9a3dd,0x00000000000000000000000003232b5ee80369a88620615f8328beec1884b731]
- withDelegatecalls: [true,true,true,true]
- startBlock: 18223833
- endBlock: 18243033
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x813261d85ca6092337de2d636c5cddac499b0db3fe19a823062b45fcc19719da
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/327.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/327.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/327_Polygon_pending_1.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/327_Polygon_pending_1.md)

**Arbitrum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/327_Arbitrum_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/327_Arbitrum_pending_0.md)


**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/327_Optimism_pending_2.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/327_Optimism_pending_2.md)

<br>

### Technical analysis

We have verified that, as presented in the specification, the following payloads properly update the variable slope 1 of WETH on all the target instances to **3.3%**.

[Polygon](https://polygonscan.com/address/0x7aa759a57c6b039a93e93683facd14209ee9a3dd#code#F1#L76)

[Arbitrum](https://arbiscan.io/address/0x1cdb984008dcee9d06c28654ed31cf82680eea62#code#F1#L26)

[Optimism](https://optimistic.etherscan.io/address/0xfc7b55cc7c5bd3ae89ac679c7250ab30754c5cc5#code#F1#L51)

[Metis](https://andromeda-explorer.metis.io/address/0x03232b5ee80369A88620615f8328BeEC1884b731/contracts#address-tabs). Due to (most probably) infrastructure issues, the payload is not verified, but we have double checked the origin repository of the proposal, and the payload is correct.


*It is important to highlight that the claim of doing it in all instances of Aave apart from Aave v3 Ethereum is incorrect, as Aave v3 Base is not affected*


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.


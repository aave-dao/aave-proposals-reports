# Proposal 392. Treasury Management - Stablecoins consolidation

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=392](https://app.aave.com/governance/proposal/?proposalId=392)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-funding-update/15194](https://governance.aave.com/t/arfc-aave-funding-update/15194)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal looks to consolidate different stablecoins held be the Aave Ethereum and Polygon Collectors into those required to cover different DAO expenses, like service providers.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x57718a4a3d001053650a7bc7cad69fd9542b2bb2ef7a20253296f0eff968e093](https://etherscan.io/tx/0x57718a4a3d001053650a7bc7cad69fd9542b2bb2ef7a20253296f0eff968e093)

```
- id: 392
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0,0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000018,0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c000000000000000000000000000000000000000000000000000000000000000e]
- withDelegatecalls: [false,false]
- startBlock: 18718824
- endBlock: 18738024
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x04ecc8577323664778b87139d2632dd33da549092d0b01a7d98dac4a0400333b
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/392.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/392.md)

**Payload reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/24.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/24.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/14.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/14.md)


<br>

### Technical analysis

The proposal has 2 different payloads, one on Ethereum and another in Polygon.

[Ethereum payload](https://etherscan.io/address/0x0B60713B53Cf01Ff53111D0BC29743eF1E03C296#code#F1#L19)

The Ethereum payload does the following:
1. Deposits 1'000'000 DAI held by the Collector into Aave v3 Ethereum on its behalf.
2. Migrates all the aDAI v2 balance held by the Collector into aDAI v3.
3. Creates an order to swap 500'000 DAI of the Collector into GHO, by using the AaveSwapper contract. The recipient will be once again the Aave Collector.
4. Withdraws all the aTUSD v2 and aBUSD v2 held by the Aave Collector, and creates orders to swap them to GHO. The recipient will be once again the Aave Collector.
5. Creates orders to swap all the UST and GUSD held by the Aave Collector into USDC. The recipient will be once again the Aave Collector.

As with previous proposals, the swaps will not be done at execution time of this payload, but afterwards, given the off-chain nature of CowSwap and Milkman.

<br>

[Polygon payload](https://polygonscan.com/address/0x6a226aF2eC3B4B40A669469c1DE48eD26CAB4607#code#F1#L19)

The Polygon payload does the following:
1. Withdraws 1'700'000 USDC from Aave v2 Polygon, and bridges it to the Ethereum Collector via the [Aave DAO <> Polygon bridge contract](https://polygonscan.com/address/0x1C2BA5b8ab8e795fF44387ba6d251fa65AD20b36).
2. Withdraws 750'000 USDT from Aave v2 Polygon, and bridges it to the Ethereum Collector via the Aave DAO <> Polygon bridge contract.
3. Withdraws 500'000 DAI from Aave v2 Polygon, and bridges it to the Ethereum Collector via the Aave DAO <> Polygon bridge contract.

<br>

---

<br>

We have verified that the proposal properly tested both the swaps and bridging operations, in environments as close as possible to production.

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

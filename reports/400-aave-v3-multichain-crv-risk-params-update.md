# Proposal 400. Aave v3 Ethereum, Polygon - CRV risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=400](https://app.aave.com/governance/proposal/?proposalId=400)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gauntlet-recommendation-to-re-enable-crv-borrowing-on-v3-ethereum-polygon/15513](https://governance.aave.com/t/arfc-gauntlet-recommendation-to-re-enable-crv-borrowing-on-v3-ethereum-polygon/15513)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal re-enables CRV for borrowing in Aave v3 Ethereum and Polygon, modifying its caps, including the debt ceiling on Aave v3 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4ab64dff48b0bbcdd9c94d72908d8bd768e432d38c8e54d6e570c9e71564343a](https://etherscan.io/tx/0x4ab64dff48b0bbcdd9c94d72908d8bd768e432d38c8e54d6e570c9e71564343a)

```
- id: 400
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0,0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec5000000000000000000000000000000000000000000000000000000000000001f,0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c0000000000000000000000000000000000000000000000000000000000000012]
- withDelegatecalls: [false,false]
- startBlock: 18753708
- endBlock: 18772908
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x3e5d25aeb435c745ac7418fea54def41da49634977153978455d5e4eef85a38d
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/400.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/400.md)


**Payloads reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/31.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/31.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/18.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/18.md)


<br>

### Technical analysis

The proposal contains 2 payloads, one for Ethereum and another for Polygon.


[v3 Ethereum](https://etherscan.io/address/0x78aCeC1B92dF516DA14B3dbed91219772180330A#code#F1#L15)

We have verified correctly uses the BGD config engine, to do the following:
- Re-enable borrowing of CRV, by setting the `borrowingEnabled` flag to `true`.
- Supply cap: 51'000'000 CRV -> **7'500'000 CRV**
- Borrow cap: 7'700'000 CRV -> **5'000'000 CRV**
- Debt ceiling: 5'000'000 USD -> **1'000'000 USD**

<br>

[v3 Polygon](https://polygonscan.com/address/0x78aCeC1B92dF516DA14B3dbed91219772180330A#code#F1#L15)

We have verified correctly uses the BGD config engine, to do the following:
- Re-enable borrowing of CRV, by setting the `borrowingEnabled` flag to `true`.
- Borrow cap: 900'190 CRV -> **300'000 CRV**

<br>

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

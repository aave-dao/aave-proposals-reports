# Proposal 254. Chaos Labs engagement payment

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=254](https://app.aave.com/governance/proposal/?proposalId=254)

<br>

### Governance forum discussion
[https://governance.aave.com/t/arfc-chaos-labs-payment-collection-request/13792](https://governance.aave.com/t/arfc-chaos-labs-payment-collection-request/13792)

<br>

## BGD analysis

<br>

### Proposal types

:money_with_wings: funds-release

<br>

### Context

This proposal releases 6'541 AAVE to a Chaos Labs controlled address, as the final payment leg of their engagement with the Aave DAO.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0xda8508321ffa4d339454bf3f592a3084e418d45ac548edaaf1234217f32bb18d](https://etherscan.io/tx/0xda8508321ffa4d339454bf3f592a3084e418d45ac548edaaf1234217f32bb18d)

```
- id: 254
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xcfff816b036423beeadc20a147586168d88b7cda]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17585764
- endBlock: 17604964
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x0238d88c03f9a1b2df8c070ff240799e114e175bd73119744d0536e4d6b066f7
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/254.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/254.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xcfff816b036423beeadc20a147586168d88b7cda#code#F1#L14) effectively transfers 6'541 AAVE from the Ecosystem Reserve by interacting with the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code), via the `transfer()` function.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

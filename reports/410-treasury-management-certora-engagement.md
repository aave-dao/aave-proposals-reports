# Proposal 410. Treasury Management - Certora engagement

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=410](https://app.aave.com/governance/proposal/?proposalId=410)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-continuous-security-proposal-aave-certora/15732](https://governance.aave.com/t/arfc-continuous-security-proposal-aave-certora/15732)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal approves a 270-days engagement for Aave with Certora, for a total of approximately $1'500'000.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6cf7e65a44e9b0921264b7853e44524dd6cf917a1e94cc5a507c7498bd64dc20](https://etherscan.io/tx/0x6cf7e65a44e9b0921264b7853e44524dd6cf917a1e94cc5a507c7498bd64dc20)

```
- id: 410
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0xea052842b3956d42883cbe8843449852b9c31dce]
- values: [0,0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40)),execute()]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000028,0x]
- withDelegatecalls: [false,true]
- startBlock: 18797533
- endBlock: 18816733
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x6646ebbf02cd4eaeae9a2dd54a6db4927503f22e45fb7495f394f2f8a55fab8c
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/410.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/410.md)

**Payloads reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/40.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/40.md)


<br>

### Technical analysis

The proposal has 2 payloads, one for the Aave Ethereum Collector stream creation, and another for the AAVE stream on the Aave Ecosystem Reserve.

[Collector payload](https://etherscan.io/address/0xa9d439364f425E22EF04e71beF7647464774D551#code#F1#L14)

The payload creates a 270-days ~1'000'000 GHO stream to the address defined as `CERTORA_TREASURY`, starting from the moment of proposal execution.

<br>


[Aave Ecosystem Reserve payload](https://etherscan.io/address/0xea052842b3956d42883cbe8843449852b9c31dce#code#F1#L17)

The payload creates a 270-days ~5'200 AAVE stream to the address defined as `CERTORA_TREASURY`, starting from the moment of proposal execution.

The ~5'200 is calculated from a 30-days average, which seems to be approximately the $500'000 requested.

<br>

We have confirmed the amount and duration is consistent with what is defined on the Aave governance forum, Snapshot and AIP.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

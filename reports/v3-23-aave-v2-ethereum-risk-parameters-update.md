# V3. Proposal 23. Aave v2 Ethereum - Risk parameters update

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=23](https://vote.onaave.com/proposal/?proposalId=23)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-v2-ethereum-lt-reductions-01-30-2024/16468](https://governance.aave.com/t/arfc-v2-ethereum-lt-reductions-01-30-2024/16468)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates multiple risk parameters on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x77ac80eef3db0b493b644615b53c220cbb82600b4f412888f80710d7ce419e56](https://etherscan.io/tx/0x77ac80eef3db0b493b644615b53c220cbb82600b4f412888f80710d7ce419e56)


```
- proposalId: 23
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xd26c294080aa7bf96dc3f291b00ca4bf57586b3977724a90a4e7cf46ef98741c
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdabad81af85554e9ae636395611c58f7ec1aaec5",
      "payloadId": "59"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0xd26c294080aa7bf96dc3f291b00ca4bf57586b3977724a90a4e7cf46ef98741c"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/23.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/23.md)

**Payloads report**

**Ethereum**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/59.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/59.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x8C56419f15734b51E3Ca6D6547393914311ab44C#code#F1#L1) updates the following parameters on Aave v2 Ethereum, via its Pool Configurator contract:

UNI
- Liquidation Threshold: 20% -> **14%**

LINK:
- Liquidation Threshold: 74% -> **72%**

MKR
- Liquidation Threshold: 18% -> **14%**

ENS
- Liquidation Threshold: 24% -> **0.05%**

CRV:
- Liquidation Threshold: 18% -> **14%**

ZRX
- Liquidation Threshold: 12% -> **8%**

<br>

The proposal payload is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

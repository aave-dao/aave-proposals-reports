# V3. Proposal 4. Aave v2 Ethereum - Risk parameters update

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=4](https://vote.onaave.com/proposal/?proposalId=4)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-v2-ethereum-lt-reductions-01-02-2024/16030#aave-v2-ethereum-4](https://governance.aave.com/t/arfc-v2-ethereum-lt-reductions-01-02-2024/16030#aave-v2-ethereum-4)

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

Transaction: [https://etherscan.io/tx/0xcecde0d40cdc23c66780390c72a49cc793f17dd357bc2f046e6915dfde3de132](https://etherscan.io/tx/0xcecde0d40cdc23c66780390c72a49cc793f17dd357bc2f046e6915dfde3de132)


```
- proposalId: 4
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x6f9c36de2cb41a1fadfe2f679c47eba6ac4c735de8ee12d3fa5b0d2b6fc3e29e
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdabad81af85554e9ae636395611c58f7ec1aaec5",
      "payloadId": "45"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0x6f9c36de2cb41a1fadfe2f679c47eba6ac4c735de8ee12d3fa5b0d2b6fc3e29e"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/4.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/4.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/45.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/45.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xE477a9F7848cF2d40FE42bB47bB1c54D3416b810#code#F1#L13) updates the following parameters on Aave v2 Ethereum, via its Pool Configurator contract:

UNI
- Liquidation Threshold: 40% -> **20%**

LINK:
- Liquidation Threshold: 75% -> **74%**

MKR
- Liquidation Threshold: 26% -> **18%**

ENS
- Liquidation Threshold: 30% -> **24%**

CRV:
- Liquidation Threshold: 25% -> **18%**

ZRX
- Liquidation Threshold: 18% -> **12%**

<br>

The proposal payload is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

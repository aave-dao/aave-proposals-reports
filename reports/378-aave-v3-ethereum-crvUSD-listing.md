# Proposal 378. Aave v3 Ethereum - listing of crvUSD

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=378](https://app.aave.com/governance/proposal/?proposalId=378)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-crvusd-onboarding-on-aave-v3-ethereum-pool/15161](https://governance.aave.com/t/arfc-crvusd-onboarding-on-aave-v3-ethereum-pool/15161)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists crvUSD (Curve.fi USD Stablecoin) on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc2ee313cb29f62279bdf41b3dd45cf6b844cd523328de63d9c3b96fe9bb76804](https://etherscan.io/tx/0xc2ee313cb29f62279bdf41b3dd45cf6b844cd523328de63d9c3b96fe9bb76804)

```
- id: 378
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000013]
- withDelegatecalls: [false]
- startBlock: 18630124
- endBlock: 18649324
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x36761f3b362b7462b1697600f0003795e4dea7a5daeb2080f00980542401f1c3
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/378.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/378.md)


**Payload report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/19.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/19.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x333b081caaD6B94697a1C06560EE336f41338110#code#F1#L18) correctly uses the BGD's Aave Config Engine of Aave v3 Ethereum, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the crvUSD listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 5%
  - Variable borrow slope 2: 80%
  - Optimal point: 80%

- The asset is not enabled as collateral
- Reserve Factor: 10%
- Supply cap: 60'000'000 crvUSD
- Borrow cap: 50'000'000 crvUSD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is a [Chainlink crvUSD/USD](https://etherscan.io/address/0xEEf0C605546958c1f899b6fB336C20671f9cD49F#readContract#F8).

The initial configuration is completely aligned with the [pre-approved by the community on Snapshot](https://snapshot.org/#/aave.eth/proposal/0xbc10b43fccd3954f02c9df774ba6f8335268727b999660738ae37a1b9d5b969e)


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

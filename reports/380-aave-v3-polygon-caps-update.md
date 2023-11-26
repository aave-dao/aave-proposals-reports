# Proposal 380. Aave v3 Polygon - Caps update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=380](https://app.aave.com/governance/proposal/?proposalId=380)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gauntlet-cap-recommendations-for-polygon-v3-2023-11-03/15327](https://governance.aave.com/t/arfc-gauntlet-cap-recommendations-for-polygon-v3-2023-11-03/15327)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal sets supply and borrow caps for agEUR and jEUR on Aave v3 Polygon.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xf8bee9282ba8d8170e57d64d22ce9e5e92ef9658c35e2698cd2ed1bdb23ef592](https://etherscan.io/tx/0xf8bee9282ba8d8170e57d64d22ce9e5e92ef9658c35e2698cd2ed1bdb23ef592)

```
- id: 380
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c000000000000000000000000000000000000000000000000000000000000000c]
- withDelegatecalls: [false]
- startBlock: 18633026
- endBlock: 18652226
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x4ac48ef13a739822e2ca321f731b123bfa6f25bb825a7fd88a48a54ad5fc41ef
```

<br>

### Aave Seatbelt reports

**Proposal report**

[https://raw.githubusercontent.com/bgd-labs/seatbelt-for-ghosts/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/380.md](https://raw.githubusercontent.com/bgd-labs/seatbelt-for-ghosts/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/380.md)

**Payload report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/12.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/12.md)

<br>

### Technical analysis

From a technical perspective, we have verified the [proposal payload](https://polygonscan.com/address/0x822d0b61d7d79d0AC2170D0A5bd634d7E11df06e#code#F1#L14) correctly uses the BGD's Aave Config Engine of Aave v3 Polygon, in this case, to update the following caps:

jEUR
- Supply cap: No cap -> **120'000 jEUR**
- Borrow cap: No cap -> **100'000 jEUR**

agEUR
- Supply cap: No cap -> **300'000 agEUR**
- Borrow cap: No cap -> **250'000 agEUR**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

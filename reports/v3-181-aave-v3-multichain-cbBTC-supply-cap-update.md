# Proposal 181. Increase cbBTC Supply Caps.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=181](https://vote.onaave.com/proposal/?proposalId=181)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-cbbtc-supply-caps-on-aave-v3-ethereum-market-and-base/19304](https://governance.aave.com/t/arfc-increase-cbbtc-supply-caps-on-aave-v3-ethereum-market-and-base/19304)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xfF7177Dd6D8adE5e0d734e632DC8f1E37e2DDdA2#code#F1#L1)

* Base - [proposal payloads](https://basescan.org/address/0xe7B862F88AcEFE43b35505a7d59df8BB868Af7AF#code#F1#L19)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the supply cap for cbBTC on V3 ethereum to 10,000 and on Base to 5,000.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd500394c26caa3eca1f4586ff5c69d33c8c89d6f4e9bf448fef6c93c1839ef81](https://etherscan.io/tx/0xd500394c26caa3eca1f4586ff5c69d33c8c89d6f4e9bf448fef6c93c1839ef81)

```
- proposalId: 181
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x06d6d7686462a0dbd65c8e167cef8507412ebae762b3aef313568113a7766543
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "190" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "41" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x06d6d7686462a0dbd65c8e167cef8507412ebae762b3aef313568113a7766543" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/181.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/181.md)

**Payload reports**

* Ethereum - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/190.md)

* Base - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/41.md)

<br>

### Technical analysis

We have confirmed that the payload successfully updates the supply cap of cbBTC on V3 ethereum mainet and BASE to 10,000 and 5,000 respectively. 

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


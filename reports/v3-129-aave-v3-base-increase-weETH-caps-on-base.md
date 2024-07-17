# Proposal 129. Increase weETH Caps on Base.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=129](https://vote.onaave.com/proposal/?proposalId=129)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-supply-and-borrow-caps-for-weeth-on-base/18248](https://governance.aave.com/t/arfc-increase-supply-and-borrow-caps-for-weeth-on-base/18248)

<br>

### Payloads

* Base - [proposal payloads](https://basescan.org/address/0xBA9020937281d05b0E0D68A0e25028C192020A6b#code#F1#L2)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal will increase the borrow and supply cap of weETH in V3 Base Market to accommodate growing demand and participate in Superchain rewards programs.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3071a7bbd204e2359c3466076cd02213b7996002a8780826327b0000332c7e89](https://etherscan.io/tx/0x3071a7bbd204e2359c3466076cd02213b7996002a8780826327b0000332c7e89)

```
- proposalId: 129
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x67a32937b865a4946846cd9a264ce83992e74ca4b60d32263b5195d38214a747
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "23" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x67a32937b865a4946846cd9a264ce83992e74ca4b60d32263b5195d38214a747" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/129.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/129.md)

**Payload reports**

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/23.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/23.md)

<br>

### Technical analysis

We have verified that the payload increase the borrow cap to 9000 and the supply cap to 20,000 of weETH.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


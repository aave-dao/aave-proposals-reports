# Proposal 176. Set ACI as Emission Manager for USDS, aUSDS and awstETH.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=176](https://vote.onaave.com/proposal/?proposalId=176)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-set-aci-as-emission-manager-for-liquidity-mining-programs/17898/17](https://governance.aave.com/t/arfc-set-aci-as-emission-manager-for-liquidity-mining-programs/17898/17)

<br>

### Payloads

* Ethereum - [proposal payloads](hhttps://etherscan.io/address/0x08afCCeDD33E41b5Dec14620ea323f9BEEec4091#code#F1#L29)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal appoint the Aave-Chan Initiative (ACI) as the Emission Manager for USDS, aUSDS and awstETH on Aave Ethereum Main & Lido instances.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1284cccade7ba96143260d9a8c0d4234ad99adcb6119783c7084e9069965245c](https://etherscan.io/tx/0x1284cccade7ba96143260d9a8c0d4234ad99adcb6119783c7084e9069965245c)

```
- proposalId: 176
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xf293a5f6cd67782e7cf2e57e8f443c062f6faa34f0647581a9eb635c448d80d8
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
      "payloadId": "185" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xf293a5f6cd67782e7cf2e57e8f443c062f6faa34f0647581a9eb635c448d80d8" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/176.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/176.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/185.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/185.md)

<br>

### Technical analysis

We have verified that the ACI multisig address was set to be the emission manager of USDS aUSDS and awstETH on the Ethereum network and Lido Instance.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


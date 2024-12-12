# Proposal 215. Onboard rsETH to Lido Instance


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=215](https://vote.onaave.com/proposal/?proposalId=215)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-rseth-to-aave-v3-ethereum/17696/18](https://governance.aave.com/t/arfc-add-rseth-to-aave-v3-ethereum/17696/18)

<br>

### Payloads

* Ethereum Lido - [proposal payloads](https://etherscan.io/address/0xD1BD2F452D79A77cd7986c50D573111B8e0D6e49#code)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

:handshake: permission granting or revoking

<br>

### Context

This proposal aims to onboard rsETH to the Aave v3 Lido instance, enabling it as a collateral asset to deepen liquidity and enhance capital efficiency for users. It includes precise risk parameters, e-mode integration with wstETH, and measures like a seed deposit to prevent first-deposit attacks. The initiative aligns with Aave’s broader strategy for supporting liquid staking derivatives (LSDs) while maintaining a conservative risk approach.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc4ffc255c6054066e95b541ce89df020be6181e864eb86f1705f24238c820441](https://etherscan.io/tx/0xc4ffc255c6054066e95b541ce89df020be6181e864eb86f1705f24238c820441)

```
- proposalId: 215
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x08f666bb422c172fd4c300bc170fb9edafb9a94eee1c9d69358492fa53769d6b
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
      "payloadId": "219" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x08f666bb422c172fd4c300bc170fb9edafb9a94eee1c9d69358492fa53769d6b" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/215.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/215.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/219.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/219.md)


<br>

### Technical analysis

We compared the parameters in the proposal, verifying alignment between the IPFS and the payload. The first deposit protection was confirmed through the seed deposit mechanism. The price feed for rsETH was validated as correctly set. The e-mode configuration, including LTV, liquidation thresholds, and bonus, was accurately implemented. Lastly, the emission admin was properly assigned to both rsETH and its corresponding aToken.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


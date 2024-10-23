# Proposal 191. Onboard ezETH to Aave V3 Lido Instance

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=191](https://vote.onaave.com/proposal/?proposalId=191)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-ezeth-to-aave-v3-lido-instance/18504](https://governance.aave.com/t/arfc-onboard-ezeth-to-aave-v3-lido-instance/18504)

<br>

### Payloads

* EthereumLido - [proposal payloads](https://etherscan.io/address/0x8c5b1D6E20B1F6584F4ADC1Ef4EfbDA5a2C1ac55#code#F1#L28)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboards exETH to the Aave v3 Lido Instance. Configures new emodes for ezETH, USDS & wstETH. Increases the borrow cap of wstETH.
<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x17a00ee6437a4b4c0f207fc7c26c27d1fb9de21499777b27662501e4a6f1a3f9](https://etherscan.io/tx/0x17a00ee6437a4b4c0f207fc7c26c27d1fb9de21499777b27662501e4a6f1a3f9)

```
- proposalId: 191
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x29e6523f02dbee892a4c9258f2b3b7992859c9ad758d5117813321e66c51486e
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
      "payloadId": "198" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x29e6523f02dbee892a4c9258f2b3b7992859c9ad758d5117813321e66c51486e" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/191.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/191.md)

**Payload reports**

* EthereumLIdo - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/198.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/198.md)

<br>

### Technical analysis

We have verified that the payloads lists ezETH on Lido Pool with the parameters mentioned in the IPFS. The emode for the specified assets has been configured correctly and the borrow cap for wstETH increased to 14,000.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


# Proposal 150. Merit Base Incentives and Superfest Matching.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=150](https://vote.onaave.com/proposal/?proposalId=150)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-merit-base-incentives-and-superfest-matching/18450](https://governance.aave.com/t/arfc-merit-base-incentives-and-superfest-matching/18450)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4EAB08d4dB0E969547F79F7fA9081ae3598F86F7#code)

* Base - [proposal payloads](https://basescan.org/address/0xac990feC479Fc94fc6EE1480261f7729E73DcAfe#code)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

:handshake: permission granting or revoking

<br>

### Context

This proposal does the following:
* grants a payment of 200,000 USDC to the ACI treasury form the mainnet collector
* grants a payment of 80,000 USDC and 20,000 USDbC to the ACI treasury form the base collector
* Grants the ACI treasury (0xac140648435d03f784879cd789130F22Ef588Fcd) the role of emission_admin for the USDC, aUSDC, wETH and aWETH tokens 


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8e63b499bc44a42e59251575777b458e9b60c6ff58e11f83b64d240eb2299043
](https://etherscan.io/tx/0x8e63b499bc44a42e59251575777b458e9b60c6ff58e11f83b64d240eb2299043
)

```
- proposalId: 150
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x1ccede5c2d46b05d034ed2c55dbb83dea3a9316df7de20fd6c365bf79bbfe413
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
      "payloadId": "161" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "30" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x1ccede5c2d46b05d034ed2c55dbb83dea3a9316df7de20fd6c365bf79bbfe413" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/150.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/150.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/161.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/161.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/30.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/30.md)
<br>

### Technical analysis

We have verified that the payloads carry out the following actions:

- grants a payment of 200,000 USDC to the ACI treasury form the mainnet collector 

- grants a payment of 80,000 USDC and 20,000 USDbC to the ACI treasury form the base collector.

- Grants the ACI treasury (0xac140648435d03f784879cd789130F22Ef588Fcd) the role of emission_admin for the USDC, aUSDC, wETH and aWETH tokens.


<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


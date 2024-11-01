# Proposal 194. stkGHO Incentives Renewel.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=194](https://vote.onaave.com/proposal/?proposalId=194)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-safety-module-stkgho-re-enable-rewards/19626](https://governance.aave.com/t/arfc-safety-module-stkgho-re-enable-rewards/19626)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xc10a383504080bE4Df3aE5Be22Ff1d428b7134F9#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal re-enables stkGHO incentive emissions for 180 days at 100 AAVE per day, after the previous period ended, to support the GHO peg and pave the way for future GHO supply expansion. It also includes approximately 2,750 AAVE from prior unclaimable emissions due to an earlier accounting error.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0e7499b8c12a362b0da81ab7a690945e5def4c45cc7363dd41e2168f7dffa165](https://etherscan.io/tx/0x0e7499b8c12a362b0da81ab7a690945e5def4c45cc7363dd41e2168f7dffa165)

```
- proposalId: 194
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x1fc2a909781193c3e9bfe527e6c1f824547e279024ed1a8685d42dde32a7933d
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
      "payloadId": "201" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x1fc2a909781193c3e9bfe527e6c1f824547e279024ed1a8685d42dde32a7933d" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/194.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/194.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/201.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/201.md)

<br>

### Technical analysis

We have verified that the contract executes the following actions:

	1.	Sets a new allowance to STK_GHO of 100 AAVE per day for 180 days.
	2.	Includes prior unclaimable emissions (~2,750 AAVE) in the allowance.
	3.	Sets the distribution end date to 180 days from the execution date.

This ensures that stkGHO incentives are re-enabled as intended, supporting the GHO peg and future GHO supply expansion.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

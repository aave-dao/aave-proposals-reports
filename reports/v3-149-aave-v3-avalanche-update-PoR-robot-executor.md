# Proposal 149. Update PoR Executor V3 Robot.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=149](https://vote.onaave.com/proposal/?proposalId=149)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/42](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/42)

<br>

### Payloads

* Avalanche Step 1 - [proposal payloads](https://snowtrace.io/address/0x8B5e80b35F89a10A9C91d129096986749c82aD9a/contract/43114/code)

* Avalanche Step 2 - [proposal payloads](https://snowtrace.io/address/0x634616a8f9D211ABb9E178BC1CD2FfE67824d750/contract/43114/code)

<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal carries out the following actions:
* Cancels the Aave Robot automation for PoR on avalanche
* Grants RISK_ADMIN rights to a new PoR executor contract
* Withdraws LINK funds from the old PoR robot
* Adds a new PoR robot
* Funds the new PoR robot with 15 LINK


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xfbc816b4a6e57619ce9ccfbe71a5d1b7d8471aa20413dae7e4c4fc0ca74a6ae0](https://etherscan.io/tx/0xfbc816b4a6e57619ce9ccfbe71a5d1b7d8471aa20413dae7e4c4fc0ca74a6ae0)

```
- proposalId: 149
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x6829dc471963cda9a2184fef9531967e9e095312995926148144a9555c3a72fd
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "47" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "48" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x6829dc471963cda9a2184fef9531967e9e095312995926148144a9555c3a72fd" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/149.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/149.md)

**Payload reports**

* Avalanche Step 1 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/47.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/47.md)

* Avalanche Step 2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/48.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/48.md) - seatbelt reverts because the first payload needs  to go through and remove the existing PoR robot before a new one can be added.

<br>

### Technical analysis

We have verified that the payload Cancels the Robot 0x7aE2930B50CFEbc99FE6DB16CE5B9C7D8d09332C on the Avalanche. We have also checked the payloads registers the robot 0x7aE2930B50CFEbc99FE6DB16CE5B9C7D8d09332C on Avalanche. 

The proposal adds a Proof of Reserve Executor 0xB94e515615c244Ab25f7A6e592e3Cb7EE31E99F4 and grands it the RISK_ADMIN role.

We have also checked the proposal funds the new PoR robot with 15 LINK.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

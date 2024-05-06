# Proposal 97. Aave v3.1 Cantina competition.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=97](https://vote.onaave.com/proposal/?proposalId=97)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-bgd-aave-3-1-cantina-competition/17485](https://governance.aave.com/t/arfc-bgd-aave-3-1-cantina-competition/17485)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x723E0347a832772a413FecC989F92a26c42f4A77#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is for the Aave DAO to have a Cantina security competition for the upcoming Aave v3.1 upgrade, to complement the other security procedures already completed. The budget of the competition will be a total of $195,000, which includes $150,000 prize pool and $45,000 allocated to platform and judging fees.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x054eec07e58d2001622ad1a244fe8f159bf289ab6b9ddc4507d0abc381c3dfd5](https://etherscan.io/tx/0x054eec07e58d2001622ad1a244fe8f159bf289ab6b9ddc4507d0abc381c3dfd5)

```
- proposalId: 97
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x831cacf552f39414ff3d30503666872f3e76d4bfdab01f3893a856496060b0ee
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
      "payloadId": "119" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x831cacf552f39414ff3d30503666872f3e76d4bfdab01f3893a856496060b0ee" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/97.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/97.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/119.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/119.md)

<br>

### Technical analysis

We have verified that the payload is transferring 195,000$ of GHO to a wallet designed by Cantina 0x3Dcb7CFbB431A11CAbb6f7F2296E2354f488Efc2.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

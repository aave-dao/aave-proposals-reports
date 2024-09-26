# Proposal 174. Upadte Flash Borrowers addresses across various instances of Aave v3.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=174](https://vote.onaave.com/proposal/?proposalId=174)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-cian-protocol-to-flashborrowers/18731/2](https://governance.aave.com/t/arfc-add-cian-protocol-to-flashborrowers/18731/2)

<br>

### Payloads

* Ethereum Mainet - [proposal payloads](https://etherscan.io/address/0x1b8874622C5C848dA78CA8e16EF29068EFc17c82#code#F1#L6)

* Ethereum Lido - [proposal payloads](https://etherscan.io/address/0x14eFcD9fE00dda2F3e0553ca031bbE1a5Ce19777#code#F1#L11)

* Ethereum EtherFi - [proposal payloads](https://etherscan.io/address/0x13756E835C05dA2a10C810A94c00cE8EF499f4cB#code#F1#L17)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x926FA1ED0B687b443b6f7fE614e04F9F7CeAe9f5#code#F1#L8)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x926FA1ED0B687b443b6f7fE614e04F9F7CeAe9f5#code#F1#L18)


<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal updates updates whitelisted flashBorrowers addresses across various instances of Aave v3.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8ebb7056ad5cc3cb026125665bce216002e7bbcf42a91a6424e7ca4a89b4a6cb](https://etherscan.io/tx/0x8ebb7056ad5cc3cb026125665bce216002e7bbcf42a91a6424e7ca4a89b4a6cb)

```
- proposalId: 174
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x30f32410de932d82dece0524b7dc1b731b7f140b43b7525715b839b7e4a35c4c
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
      "payloadId": "181" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "51" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "53" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x30f32410de932d82dece0524b7dc1b731b7f140b43b7525715b839b7e4a35c4c" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/174.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/174.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/181.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/181.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/51.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/51.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/53.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/53.md)


<br>

### Technical analysis

We have verified that the code correctly adds the specified flash borrowers, including CIAN, Index Coop, and Contango, to the Aave V3 ACL managers on the appropriate networks and instances as requested.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

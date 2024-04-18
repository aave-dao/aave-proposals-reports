# Proposal 78. Optimism susd Emission Admin.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=78](https://vote.onaave.com/proposal/?proposalId=78)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-set-aave-chan-initiative-as-emission-manager-for-susd-on-aave-v3-optimism/16867](https://governance.aave.com/t/arfc-set-aave-chan-initiative-as-emission-manager-for-susd-on-aave-v3-optimism/16867)

<br>

### Payloads

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x2BED3B908c98b315ae5cbF601918739646c74482#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal propose to set an emission manager for sUSD on Optimism chain to incentivize growth of Aave v3 on the Optimism chain.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9b40b659506dc0236c4e41742a269aedecc2e65b5799e3389ebeffd3268b461d](https://etherscan.io/tx/0x9b40b659506dc0236c4e41742a269aedecc2e65b5799e3389ebeffd3268b461d)

```
- proposalId: 78
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x4041602937f71b639d1eeb894e051c552152cf418d95ee4799a6ba893a6b0b13
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "25" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x4041602937f71b639d1eeb894e051c552152cf418d95ee4799a6ba893a6b0b13" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/78.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/78.md)

**Payload reports**

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/25.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/25.md)

<br>

### Technical analysis

We have verified that the payload is setting a declared ACI multisig as the emission admin of sUSD over the Optimism chain and has no further side effects.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

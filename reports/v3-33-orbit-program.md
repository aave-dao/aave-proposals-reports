# Proposal 33. Orbit Program.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=33](https://vote.onaave.com/proposal/?proposalId=33)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-orbit-program-renewal/16550](https://governance.aave.com/t/arfc-orbit-program-renewal/16550)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xE15a36c5Cc282C62539a8772A2fcb293E7D2aa14#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer
:bank: payment stream

<br>

### Context

This proposal renewals the Orbit program for recognized delegates, Compensating them with GHO and ETH reimbursement of Gas costs associated with their governance activity.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe63c8691946f9f68326b4ca2ee6cefbde9745c989c5c0155ecc0136a569a215b](https://etherscan.io/tx/0xe63c8691946f9f68326b4ca2ee6cefbde9745c989c5c0155ecc0136a569a215b)

```
- proposalId: 33
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x56181ff7b11d3dca7c8a50c6cd63aed6a8367179f1a745060c1d146535a9180e
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
      "payloadId": "64" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x56181ff7b11d3dca7c8a50c6cd63aed6a8367179f1a745060c1d146535a9180e" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/33.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/33.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/64.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/64.md)

<br>

### Technical analysis

We have verified that the payload executes the following actions:

- transfer 5,000 GHO to each of the following addresses: 
    1-0x0579a616689f7ed748dc07692a3f150d44b0ca09 - Michigan.

    2-0x8659d0bb123da6d16d9394c7838ba286c2207d0e - ezr3al.

    3-0x8b37a5af68d315cf5a64097d96621f64b5502a22 - LBS Blockchain.

    4-0xecc2a9240268bc7a26386ecb49e1befca2706ac9 - Stable Labs.

- create payment stream of 15,000 GHO during a duration of 90 days to each of the following addresses: 
    1-0x0579a616689f7ed748dc07692a3f150d44b0ca09 - Michigan.

    2-0x8659d0bb123da6d16d9394c7838ba286c2207d0e - ezr3al.

    3-0x8b37a5af68d315cf5a64097d96621f64b5502a22 - LBS Blockchain.

    4-0xecc2a9240268bc7a26386ecb49e1befca2706ac9 - Stable Labs.

- transfer a sum of 4.9273 ETH to the following service providers:
    1-0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922 - ACI - 3.365 ETH.

    2-0x2cc1ADE245020FC5AAE66Ad443e1F66e01c54Df1 - Tokenlogic - 0.586 ETH.

    3-0x0579a616689f7ed748dc07692a3f150d44b0ca09 - Michigan - 0.276 ETH.

    4-0xB933AEe47C438f22DE0747D57fc239FE37878Dd1 - Wintermute - 0.2518 ETH.

    5-0x8b37a5Af68D315cf5A64097D96621F64b5502a22 - LBS - 0.031 ETH.

    6-0xECC2a9240268BC7a26386ecB49E1Befca2706AC9 - StableLabs - 0.0342 ETH.

    7-0x8659D0BB123Da6D16D9394C7838BA286c2207d0E - ezr3al - 0.3833 ETH.
<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

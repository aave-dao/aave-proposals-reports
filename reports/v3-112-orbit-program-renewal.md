# Proposal 112. Orbit Program Renewal.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=112](https://vote.onaave.com/proposal/?proposalId=112)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-orbit-program-renewal-may-2024/17683](https://governance.aave.com/t/arfc-orbit-program-renewal-may-2024/17683)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xD991F6f9d6513d85f2B8fa6B8Da12a3A99e3DCf1#code#F1#L1)

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

Transaction: [https://etherscan.io/tx/0x2ea2417965ffdb0f36ef7857459746b39aae3e69ad012f7d55fe55023617fc53](https://etherscan.io/tx/0x2ea2417965ffdb0f36ef7857459746b39aae3e69ad012f7d55fe55023617fc53)

```
- proposalId: 112
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xc1be7e70b05f3bcd2978bd67fff306ed55e4cecac3ac4b2bf66c334d9e8648e4
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
      "payloadId": "132" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xc1be7e70b05f3bcd2978bd67fff306ed55e4cecac3ac4b2bf66c334d9e8648e4" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/112.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/112.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/132.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/132.md)

<br>

### Technical analysis

We have verified that the payload executes the following actions:

- create payment stream of 15,000 GHO during a duration of 90 days to each of the following addresses: 

    1-0x08651EeE3b78254653062BA89035b8F8AdF924CE - Saucy Block.

    2-0x8659D0BB123Da6D16D9394C7838BA286c2207d0E - ezr3al.

    3-0x8b37a5Af68D315cf5A64097D96621F64b5502a22 - Areta.

    4-0xECC2a9240268BC7a26386ecB49E1Befca2706AC9 - Stable Labs.

- transfer a sum of 3.381 ETH to the following service providers:

    1-0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922 - ACI - 2.74 ETH.

    2-0x2cc1ADE245020FC5AAE66Ad443e1F66e01c54Df1 - Tokenlogic - 0.641 ETH.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

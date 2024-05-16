# Proposal 106. Deprecation of Small-cap Stablecoins on V2 Ethereum.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=106](https://vote.onaave.com/proposal/?proposalId=106)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-deprecation-of-small-cap-stablecoins-on-v2-ethereum/17484/1](https://governance.aave.com/t/arfc-deprecation-of-small-cap-stablecoins-on-v2-ethereum/17484/1)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x04565551453e20a0b58b890bA71CeDEea9d1Fb41#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal is the first phase of deprecation of multiple frozen stable-coins on Aave-V2-Ethereum, in order to encourage users to migrate from v2 to v3. 

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xfe41d70d2336aec8a03403ac60068dd260e61acb58190eba8a333924982d3e9a](https://etherscan.io/tx/0xfe41d70d2336aec8a03403ac60068dd260e61acb58190eba8a333924982d3e9a)

```
- proposalId: 106
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xa66007518f76400be6e37151d23bfcd8fe9b6b6a72fe5eaa2fd60bdaa2a24b22
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
      "payloadId": "128" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xa66007518f76400be6e37151d23bfcd8fe9b6b6a72fe5eaa2fd60bdaa2a24b22" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/106.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/106.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/128.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/128.md)

<br>

### Technical analysis

We have verified that the payload modifies the following parameters of USDP, GUSD, LUSD, FRAX, sUSD on Aave-V2-Ethereum:

-    Reserve Factor - 95%

-    Borrowing Enabled - No

-    Base Rate - 3%

-    Variable Slope1 - 15%

-    Variable Slope2 - 200%

-    UOptimal - 20%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

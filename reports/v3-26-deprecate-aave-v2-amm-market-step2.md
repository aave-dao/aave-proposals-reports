# Proposal 26. Deprecate Aave V2 AMM Market - Step 2.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=26](https://vote.onaave.com/proposal/?proposalId=26)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-deprecate-aave-v2-amm-market-step-2/16408/1](https://governance.aave.com/t/arfc-deprecate-aave-v2-amm-market-step-2/16408/1)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x51f92A1dE69AeEc30C113C2FD9CF8A63871C76d7#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal changes the reserve factors, Variable Bases and Variable Slope1's of the following assets on Aave-V2-EthereumAMM: DAI, USDC, USDT, wETH, wBTC, in order to encourage people to migrate from Ethereum-AMM v2 to v3.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xfb2218bb6631a1a31aeaf9eb3d8038a60cd515e155074bd258b9ef8571370a29](https://etherscan.io/tx/0xfb2218bb6631a1a31aeaf9eb3d8038a60cd515e155074bd258b9ef8571370a29)

```
- proposalId: 26
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- accessLevel: 1
- ipfsHash: 0x599229f841648a3d59bfd25079ff627f2b631856d494db31e3c219a0b53818b3
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
      "payloadId": "61"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xee81375a113564e990021db582f787e045b68d85f146e4a6dc6def36dd06ace9"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/26.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/26.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/61.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/61.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor, Variable Base and Variable Slope1 of the following tokens:

RF:

    DAI: From: 10% To: 99%

    USDC: From: 10% To: 99%

    USDT: From: 10% To: 99%

    wETH: From: 10% To: 99%

    wBTC: From: 20% To: 99%

Variable Base:

    DAI: To: 4%

    USDC: To: 4%

    USDT: To: 6%

    wETH: To: 6%

    wBTC: To: 5%

Variable Slope1:

    DAI: To: 10%

    USDC: To: 10%

    USDT: To: 10%

    wETH: To: 8%

    wBTC: To: 8%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

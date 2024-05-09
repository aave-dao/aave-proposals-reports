# Proposal 103. April Finance Update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=103](https://vote.onaave.com/proposal/?proposalId=103)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-april-finance-update/17390](https://governance.aave.com/t/arfc-april-finance-update/17390)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x7102305b5E55253aCA6Dc660A2eD24C8Ac87e2Cd#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xc9f0f9bd1F49B2B03367ca886Ea0cCB384643E98#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xAC7F179352b9D388067bA00bf1f0d64483e51786#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x96c0900600cc68e2EA6d1e36CEda8cB27f8C9c0E#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is a collection of treasury management actions that mainly aim to consolidate the ecosystem holdings in gho and preparing treasury for upcoming expected expenses.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x2584a9273c599b0d195707a04c40d87b460ad92139f4ef195f68b737d7d39a01](https://etherscan.io/tx/0x2584a9273c599b0d195707a04c40d87b460ad92139f4ef195f68b737d7d39a01)

```
- proposalId: 103
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xd527226735a84a4847a5096a2d861759ee5a1c33cc9fc6971d13445ab40dcc86
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
      "payloadId": "125" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "62" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "63" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "19" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xd527226735a84a4847a5096a2d861759ee5a1c33cc9fc6971d13445ab40dcc86" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/103.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/103.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/125.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/125.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/62.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/62.md)


* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/63.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/63.md) - The seatbelt reverts because the payload is dependent on the other Polygon payload to be executed first.


* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/19.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/19.md)


<br>

### Technical analysis

We have verified that the payloads are executing the following actions:

* BGD Reimbursements

1. Transfer 42,000 aUSDC v2 Ethereum to an address provided by BGD.
2. Transfer 109,200 aUSDT v2 Ethereum to an address provided by BGD.
3. Transfer 1640 aLINK v2 Ethereum to an address provided by BGD.
4. Transfer 4000 aMATIC v2 Polygon to an address provided by BGD.

* aDI BOT Refill

1. Transfer 20,000 MATIC to the aDI bot.

* Migrating AGD's allowance to GHO

1. switch aUSDT allowance to 0.
2. switch GHO allowance to 613,000.

* Merit Allowances

1. switch GHO allowance to 3,000,000.
2. switch aEthWETH allowance to 645.

* Returning RealT's supplied WXDAI to RealT

1. Transfer 3,504 armmv3WXDAI Gnosis to an address which was provided.

* Consolidate GHO funding and Migrate funds from V2 to V3

1. withdraw and swap to GHO of the following assets on Ethereum:

- aEthUSDC - 1.4M

- aDAI - (All-1)

- aUSDC - (All-1)

- aUSDT - (All-1)

- aEthDAI - (2M)

2. Migrate the following assets from V2 to V3 on Ethereum:

- awBTC - (All-1)

- awETH - (All-1)

- aLINK - (All-1)

- aSNX - (All-1)

3. Bridge the following assets from Polygon to Ethereum:

- aPolDAI - (All-1)

- amUSDC - (All-1)

- aPolMATIC - (All-40,000)

- amDAI - (All-1)

- aPolUSDC - (All-1)

- amMATIC - (All-1)

4. Migrate the following assets from V2 to V3 on Polygon:

- amUSDT - (All-1) 

<br>

The proposal is consistent with the description on the governance forum except the following:

- The amount of aEthDAI being withdrawn and swapped to GHO is 2M instead of (All-1) because there is not enough liquidity in the pool to withdraw the full amount .

- aSUSD, aPAX will not be withdrawn and and swapped to GHO since it was advised we keep those funds as they have been deprecated to users can off-board.

- The amount of aPolMATIC to be bridged is (All-40,000) instead of (All-1) in order to refill the aDI bot eventually.

- The deposit of wETH and wBTC in the Treasury into Aave v3 will happen in part B.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

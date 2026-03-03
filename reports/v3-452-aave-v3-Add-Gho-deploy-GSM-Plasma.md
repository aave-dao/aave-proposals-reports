# Proposal 452. Add GHO on Aave Plasma and deploy GSM on Plasma.

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=452)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-launch-gho-on-plasma-set-aci-as-emissions-manager-for-rewards/22994/6)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x25fE5e08CDF28C80bC89a4bF289534F9E80E205D)

* Ethereum - [proposal payloads](https://etherscan.io/address/0xE94566cF49B7D9191d8134E6C9dd07b637510cf1)

* Plasma - [proposal payloads](https://plasmascan.to/address/0x6D81A51A71c204C174e470A0979908d35162f171)

* Plasma - [proposal payloads](https://plasmascan.to/address/0x36DC7bD06d8aE30eF86c390c0342d22D7dDeE7D4)


## Certora Analysis

### Proposal Types


* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets



### Context
With the GHO lanes now activated on CCIP, this publication defines the launch parameters for GHO on Plasma, as well as the introduction of GSMs on Plasma.

### Proposal Creation
Transaction: [0x5028e5aff0a6b35ae649d7e9f2353f1aba584688fbbc8efd3dffa36690cc7987](https://etherscan.io/tx/0x5028e5aff0a6b35ae649d7e9f2353f1aba584688fbbc8efd3dffa36690cc7987)
- `proposalId`: 452
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x3053230c267a7580a607ab6f11ebd03fc1427efba557cee5ee4b294045b1fe40

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "406" 
    }, 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "407" 
    }, 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "17" 
    }, 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "18" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0x3053230c267a7580a607ab6f11ebd03fc1427efba557cee5ee4b294045b1fe40" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/452.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/406.md)

* Ethereum - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/407.md)

* Plasma - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/17.md)

* Plasma - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/18.md)


### Technical Analysis

We verified the GHO token listing parameters.

We verified all core protocol addresses, including the GHO_TOKEN, the stataUSDT RemoteGSM, and the GHO_ORACLE.

We reviewed the RemoteGSM (stataUSDT) logic, confirming the integration of the GhoDirectFacilitator on Ethereum to support the 50M GHO initial mint and the 10M initial exposure cap on Plasma to mitigate early arbitrage risk.

We verified the E-Mode category creations (GHO__USDT0, syrupUSDT__GHO, and syrupUSDT_GHO__USDT0), confirming parameters. 

We validated the payload logic and confirmed execution via Seatbelt ensuring no unintended configuration changes were made.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
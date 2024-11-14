# Proposal 200. Automated (Edge) AGRS Activation


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=200](https://vote.onaave.com/proposal/?proposalId=200)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-generalized-risk-stewards-agrs-activation/19178/6](https://governance.aave.com/t/arfc-aave-generalized-risk-stewards-agrs-activation/19178/6)

<br>

### Payloads

* EthereumLido - [proposal payloads](https://etherscan.io/address/0xfB04B9434a5CF259b9c37bFC45E9EFef55C66EAB#code)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

:moneybag: :receipt: asset transfer

<br>

### Context

With the manual Aave Generalized Risk Stewards (AGRS) already active, this proposal introduces an automated AGRS system to manage `WETH` interest rates on the Lido instance using Chaos Labs’ Edge Risk Oracle. The integration aims to maintain WETH borrowing rates below Lido’s staking rewards to support leveraged staking strategies while dynamically adjusting rates to stabilize borrowing conditions as demand fluctuates. By aligning with Lido’s staking rewards and considering utilization and E-Mode demand, the AGRS ensures stable lending and supports predictable looping strategies for users.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x73fb87b48b4d540b3b0b507c18ba82a05243fe2284f4c62826c87274a32a23bb](https://etherscan.io/tx/0x73fb87b48b4d540b3b0b507c18ba82a05243fe2284f4c62826c87274a32a23bb)

```
- proposalId: 200
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xe47e9b75f60408381485d14ff71ce9c855d7a75acc525c01c231a2ec4a130834
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
      "payloadId": "206" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xe47e9b75f60408381485d14ff71ce9c855d7a75acc525c01c231a2ec4a130834" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/200.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/200.md)

**Payload reports**

* EthereumLido - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/206.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/206.md)

<br>

### Technical analysis

In our review of Proposal 200, we conducted a comprehensive comparison between the declared intentions in the proposal documentation and the actual Solidity code. We specifically checked that the automated AGRS integration with the Edge Risk Oracle aligns with stated goals to adjust WETH interest rates dynamically based on Lido staking rewards and pool utilization. Key areas of focus included verifying that the AaveStewardInjector is appropriately authorized to update the EdgeRiskSteward and ensuring that only the WETH asset is affected, as specified.

We also examined the configuration parameters in EdgeRiskSteward to confirm alignment with the proposal’s constraints on rate adjustments for Slope1, Slope2, base rates, and utilization thresholds. In addition, we reviewed the deployment and governance setup, confirming that all necessary roles, such as the RISK_COUNCIL, are correctly assigned to allow seamless automated updates.

Lastly, we confirmed that while the proposal itself is unaffected, the address book files reference an outdated RISK_STEWARD address from before Proposal 197, which may need updating for consistency in future proposals.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


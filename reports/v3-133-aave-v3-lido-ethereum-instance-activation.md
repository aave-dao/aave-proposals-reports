# Proposal 133. Lido Ethereum Instance Activation.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=133](https://vote.onaave.com/proposal/?proposalId=133)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-deploy-a-lido-aave-v3-instance/18047](https://governance.aave.com/t/arfc-deploy-a-lido-aave-v3-instance/18047)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x683FdF51d5898F92317F870B25a6A4dF67dC58Ab#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

:gem: :new: asset-listing

:handshake: permission granting or revoking

<br>

### Context

This proposal activates the ethereumLido v3.1 instance in order to attract wETH liquidity which will benefit both Aave DAO and Lido users.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x7009d9a458b2c864729ba25ab6f864a20c27c3b70fa0a6363293ee7ab77ce5fb](https://etherscan.io/tx/0x7009d9a458b2c864729ba25ab6f864a20c27c3b70fa0a6363293ee7ab77ce5fb)

```
- proposalId: 133
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0x7b95ebeac91f0a0f3eef3670e0c9466086f270b56f662a5a0fec0457a0b5dab5
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
      "payloadId": "147"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x7b95ebeac91f0a0f3eef3670e0c9466086f270b56f662a5a0fec0457a0b5dab5"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/133.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/133.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/147.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/147.md)

<br>

### Technical analysis

We have verified that the payload activates the ethereumLido v3.1 instance with the following:

- Set Ethereum V3 Incentives Controller to manage Ethereum Lido incentives.

- Register Ethereum Lido instance in Ethereum V3 PoolAddressesProviderRegistry.

- Set Ethereum PROTOCOL_GUARDIAN as temporary Pool Admin of Ethereum Lido instance.

- Set Risk Admin to CapsPlusRisk Steward contract.

- Set ACI as emission admin of WETH and aWETH rewards for LM program.

Add eMode category of ETH correlated with the following parameters:

- LTV: 93.5%

- LT: 95.5%

- Liquidation Bonus: 1%

The following assets are added with the parameters which are specified in the IPFS and forum: 

- wstETH

- wETH

We have also verified that 15,000 GHO are sent as service fee for Catapulta deployment service provider.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


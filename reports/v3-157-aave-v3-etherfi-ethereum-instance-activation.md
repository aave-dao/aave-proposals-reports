# Proposal 133. Etherfi Ethereum Instance Activation.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=157](https://vote.onaave.com/proposal/?proposalId=157)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-deploy-an-etherfi-stablecoin-aave-v3-instance/18440](https://governance.aave.com/t/arfc-deploy-an-etherfi-stablecoin-aave-v3-instance/18440)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xee5BC1F738e8100279d293a376bF5ffE60BCDa36#code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

:gem: :new: asset-listing

:handshake: permission granting or revoking

:moneybag: :receipt: asset transfer
<br>

### Context

This proposal activates the Aave v3 EtherFi instance in order to meet the high demand for borrowing wETH on Aave using weETH as collateral.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x2300662ec66ec45800c8215857074a28a3727ed711f5d95784d52dca5e2e1d82](https://etherscan.io/tx/0x2300662ec66ec45800c8215857074a28a3727ed711f5d95784d52dca5e2e1d82)

```
- proposalId: 157
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x4fadf8fd69d0a3438ed48d6c69173bee13ab0789ef29bfd931c30adce38b8438
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
      "payloadId": "166" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x4fadf8fd69d0a3438ed48d6c69173bee13ab0789ef29bfd931c30adce38b8438" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/157.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/157.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/166.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/166.md)

<br>

### Technical analysis

We have verified that the payload activates the Aave v3 EtherFi instance with the following:

- Register Ethereum Etherfi instance in Ethereum V3 PoolAddressesProviderRegistry with ID 45.

- Set Ethereum PROTOCOL_GUARDIAN as Pool Admin of Ethereum Etherfi instance.

- Set Risk Admin to CapsPlusRisk Steward contract.

- Transfer 15,000 GHO to Catapulta as their service fee

- Listing of weETH, USDC, PYUSD, and FRAX tokens with the specified configuration

- Supply seed amount for each of the newly listed tokens

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


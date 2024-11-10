# Proposal 198. GHO CCIP Integration Maintenance


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=198](https://vote.onaave.com/proposal/?proposalId=198)

<br>

### Governance forum discussion

[https://governance.aave.com/t/technical-maintenance-proposals/15274/54](https://governance.aave.com/t/technical-maintenance-proposals/15274/54)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x375eDb6F983995a95f8d781A194A1A7903CF18A0#code)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x03549418Cb18108bA365563d7394f7a3D851014f#code)

<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade

<br>

### Context

This proposal aims to update the GHO CCIP Token Pools to ensure compatibility with the forthcoming Chainlink CCIP version 1.5 upgrade. By implementing an Intermediary Contract and upgrading the existing GHO Token Pools, the proposal facilitates a smooth transition between CCIP versions, preserving GHO’s cross-chain functionality. Additionally, a temporary token rate limit is established to enhance security during this transition. This update empowers the Aave DAO to maintain seamless cross-chain operability for GHO, supporting its growth and potential expansion to other networks.
<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x851765606ba5c8da308e8d824c57ae843a84a7f07561fb85b01e444f33700caa](https://etherscan.io/tx/0x851765606ba5c8da308e8d824c57ae843a84a7f07561fb85b01e444f33700caa)

```
- proposalId: 198
- creator: 0x66a28531e6f390a8cd44ab0c57a0f1aeb7e673ff
- accessLevel: 1
- ipfsHash: 0xedd135d40170a5acedfecf4294588144ac8d35dd4e5a6cae1975ded3537b5b61
```

<br>

**createProposal() parameters**

```

```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/198.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/198.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/204.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/204.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/60.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/60.md)

<br>

### Technical analysis

In our technical review of the GHO CCIP 1.5 upgrade proposal, we verified that the upgrade payload executed as intended, particularly focusing on key components necessary for the CCIP migration. First, we confirmed that the proxyPool was upgraded to the designated intermediary contract, ensuring the intermediate contract would facilitate communication between the legacy and new CCIP implementations. This check was essential to validate the seamless interaction required for compatibility with version 1.5.

Additionally, we inspected the configuration of the rate limiter to confirm it adheres to the specified parameters: a capacity of 300,000 GHO and a refill rate of 60 GHO per second. This configuration is critical for maintaining secure, regulated token flow across the Ethereum and Arbitrum networks, providing a safeguard against potential excess transfers during the migration phase.

Finally, we reviewed the payload as a whole to ensure all intended actions were executed properly, affirming that each element required for the upgrade—including the deployment of the intermediary contract, token pool upgrades, and rate limiter settings—was included and aligned with the proposal’s goals. This thorough review confirms that the upgrade payload fully supports the transition to CCIP version 1.5 without compromising functionality or security across the integrated networks.
<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.


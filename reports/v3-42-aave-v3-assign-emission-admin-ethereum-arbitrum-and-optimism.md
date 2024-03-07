# Proposal 42. Assign Emission Admin - Ethereum, Arbitrum and Optimism

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=42](https://vote.onaave.com/proposal/?proposalId=42)

<br>

### Governance forum discussion

* SD + ETHx - [https://governance.aave.com/t/arfc-set-ethx-and-sd-emission-admin-to-stader-labs/16599](https://governance.aave.com/t/arfc-set-ethx-and-sd-emission-admin-to-stader-labs/16599)

* SWISE + osETH - [https://governance.aave.com/t/arfc-set-oseth-swise-emission-admin-to-stakewise/16590](https://governance.aave.com/t/arfc-set-oseth-swise-emission-admin-to-stakewise/16590)

* OP - [https://governance.aave.com/t/arfc-set-op-emission-admin/16621](https://governance.aave.com/t/arfc-set-op-emission-admin/16621)

* ARB [https://governance.aave.com/t/arfc-set-arb-emission-admin-to-gauntlet/16554](https://governance.aave.com/t/arfc-set-arb-emission-admin-to-gauntlet/16554)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xbbf41C0Ba803A023DDD327A3F47468d388093942#code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x2dA3dC6a7A4f5f102a8718720C0873a4beD2a8B1#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x13374e842237b627B93ad96c5Dc4F0B49a918f80#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal sets various teams to distribute rewards across Aave v3. The below summaries each initiative:
- ETHx & SD rewards by Stader Labs on Ethereum

- osETH & SWISE by Stakewise DAO on Ethereum

- OP reward via an Aave Community SAFE on Optimism

- ARB rewards via Gauntlet on Arbitrum

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5de5e742ac4b347cded1ed982047eac17c5bbe1027437e75b09575b6ed00b66f](https://etherscan.io/tx/0x5de5e742ac4b347cded1ed982047eac17c5bbe1027437e75b09575b6ed00b66f)

```
- proposalId: 42
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xec3016442469c3ffdd667b301c35a50b0851b0bd2bff4f563a5a320e6abbdaca
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
      "payloadId": "71"
    },
    {
      "chain": "10",
      "accessLevel": 1,
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
      "payloadId": "15"
    },
    {
      "chain": "42161",
      "accessLevel": 1,
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
      "payloadId": "13"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "	0xec3016442469c3ffdd667b301c35a50b0851b0bd2bff4f563a5a320e6abbdaca"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/42.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/42.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/71.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/71.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/15.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/15.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/13.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/13.md)

<br>

### Technical analysis

We have verified that the payloads sets the following admins on the following chains:
- the address 0xbDa6C9cd7eD043CB739ca2C748dAbd1fCA397132 (Stader Labs) on SD, ETHx on Ethereum.

- the address 0x189Cb93839AD52b5e955ddA254Ed7212ae1B1f61 (Stakewise DAO) on SWISE, osETH on Ethereum.

- the address 0x3479CEb4b1fcaDC586d4c5F1c16b4d8c0D70Bc71 (Aave Community SAFE) on OP on Optimism.

- the address 0xE79C65a313a1f4Ca5D1d15414E0c515056dA90b4 (Gauntlet) on ARB on Arbitrum.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

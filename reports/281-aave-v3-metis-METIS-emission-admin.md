# Proposal 281. Aave v3 Metis - update EMISSION_ADMIN role for METIS

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=281](https://app.aave.com/governance/proposal/?proposalId=281)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-set-metis-foundation-wallet-as-emission-manager-for-metis-token-on-aave-v3-metis-pool/13912](https://governance.aave.com/t/arfc-set-metis-foundation-wallet-as-emission-manager-for-metis-token-on-aave-v3-metis-pool/13912)

<br>

## BGD analysis

<br>

### Proposal types

:gift: rewards

<br>

### Context

This proposal sets EMISSION_ADMIN role for the Metis foundation to configure rewards of METIS on Aave v3 Metis.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xcdb7405034ad3497fe8fa645756e3f461ccb9cca37341eb538ed4b610783fb5b](https://etherscan.io/tx/0xcdb7405034ad3497fe8fa645756e3f461ccb9cca37341eb538ed4b610783fb5b)

```
- id: 281
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x2fe52ef191f0be1d98459bdad2f1d3160336c08f]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000d82f30507e4cdbf63d0091d0db866f7f4b09fd90]
- withDelegatecalls: [true]
- startBlock: 17785616
- endBlock: 17804816
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x015af7b18b58de973aad4882ebbb5db758887fb25e1f462e7bce652ed4ada36f
```

<br>

### Aave Seatbelt report

**Ethereum report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/281.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/281.md)

**Metis report:**

Aave Seatbelt doesn't support Metis at the moment.


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system.

The [proposal payload](https://andromeda-explorer.metis.io/address/0xd82F30507E4cDbf63D0091d0DB866f7f4B09FD90/contracts#address-tabs) correctly interacts with the [EmissionManager of Aave v3 Metis](https://andromeda-explorer.metis.io/address/0xfDb2580A1ac4CDc67E4236738b28af59e2022Dd2/contracts#address-tabs) to set the `EMISSION_ADMIN` role to the [Gnosis Safe](https://andromeda-explorer.metis.io/address/0x97177cD80475f8b38945c1E77e12F0c9d50Ac84D), by calling `setEmissionAdmin()`.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

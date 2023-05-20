# Proposal 228 (repetition of part of 220). Aave Ethereum - AGD (Aave Grants DAO) correction of allowance


<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=228](https://app.aave.com/governance/proposal/?proposalId=228)

<br>

### Governance forum discussion

[https://governance.aave.com/t/updated-proposal-aave-grants-dao-renewal/11289/9](https://governance.aave.com/t/updated-proposal-aave-grants-dao-renewal/11289/9)

<br>

## BGD analysis

<br>

### Proposal types

:credit_card: funds-allowance

<br>

### Context

This proposal gives allowance of aUSDT Aave v2 to Aave Grants DAO, replacing the wrong allowance of aUSDT Aave v1.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb3517dc486ff23e954292dc543234302f74ff6d0b824c9bcc4939fb21e71bb13](https://etherscan.io/tx/0xb3517dc486ff23e954292dc543234302f74ff6d0b824c9bcc4939fb21e71bb13)

```
- id: 228
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x7be4fa90565d6fd6f7091d0af9e5a7f9cd7918a6]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17279524
- endBlock: 17298724
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xbf94d92c69c8818c2259010608e0c6ec2cb9d922e71a7a007cd54a3ef052230c
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/228.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/228.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x7be4fa90565d6fd6f7091d0af9e5a7f9cd7918a6#code#F6#L1) correctly reduces the allowance of aUSDT Aave v1 to 0, and replaces it with allowance of 812'944.90 aUSDT Aave v2.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

# Proposal 87. Strategic Investment Part 1 - BAL <> AAVE Token Swap

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=87](https://app.aave.com/governance/proposal/?proposalId=87)

### Governance forum discussion
[https://governance.aave.com/t/arc-strategic-partnership-with-balancer-part-1/7617](https://governance.aave.com/t/arc-strategic-partnership-with-balancer-part-1/7617)

<br>

## BGD analysis

### Proposal types

:credit_card: funds-allowance

:money_with_wings: funds-release

### Context

This proposal approves 16'907.28 AAVE to an OTC-swap smart contract, to execute a swap for 200'000 BAL with the Balancer community.

### Proposal creation
Transaction: [https://etherscan.io/tx/0x85095463129f088281c45f5bb7f87fdf8e7904e983a3c91ef851058af71983fe](https://etherscan.io/tx/0x85095463129f088281c45f5bb7f87fdf8e7904e983a3c91ef851058af71983fe)
```
- id: 87
- creator: 0x5b3bffc0bcf8d4caec873fdcf719f60725767c98
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xc730008c64783a283988b0fa3b5ee6b6f997922a]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15130276
- endBlock: 15149476
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf27eb37dc1f6129638e61204393c7f27bafa4c4f9ae4ea6170132af7f51bc7e2
```

### Aave Seatbelt report
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/087.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/087.md)

### Technical analysis

From a technical perspective, we have verified that the proposal payload does the following:

1. Approves 16'907.28 AAVE to an [OTC-swap smart contract](https://etherscan.io/address/0x5AE986d7ca23fc3519daaa589E1d38d19BA42a47#code) that contains the logic to swap this amount for 200'000 BAL. The proposer has confirmed us that this proportion is defined on a 90 days price average, disclosed to the community on the governance forum discussion, and pre-approved on Snapshot.

2. Calls the function `swap()` on the aforementioned [OTC-swap smart contract](https://etherscan.io/address/0x5AE986d7ca23fc3519daaa589E1d38d19BA42a47#code).

3. This `swap()` function 1) takes the pre-approved AAVE tokens from the [Aave ecosystem reserve](https://etherscan.io/address/0x25F2226B597E8F9514B3F68F00f494cF4f286491) and sends them to the [Balancer Treasury](https://etherscan.io/address/0x10A19e7eE7d7F8a52822f6817de8ea18204F2e4f), and takes the pre-approved BAL from the Balancer Treasury and sends them to the [Aave V2 Ethereum Collector](https://etherscan.io/address/0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c)


### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:white_check_mark: Only one payload used via delegatecall


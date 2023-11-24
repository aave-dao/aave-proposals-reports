# Proposal 375. Aave v3/v2 Ethereum, Polygon, Avalanche, Optimism, Arbitrum, Metis, Base - Stablecoins interest rate update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=375](https://app.aave.com/governance/proposal/?proposalId=375)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-optimal-borrow-rates-for-ethereum-stablecoin-markets/15096/3](https://governance.aave.com/t/arfc-increase-optimal-borrow-rates-for-ethereum-stablecoin-markets/15096/3)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates different rate strategy parameters and RF for multiple reserves across all active Aave v2 and v3 instances.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x71b4c1f181858834089d186d49947776acca911e835f391b98738afeefa9c2ce](https://etherscan.io/tx/0x71b4c1f181858834089d186d49947776acca911e835f391b98738afeefa9c2ce)

```
- id: 375
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0,0,0,0,0,0,0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000014,0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c000000000000000000000000000000000000000000000000000000000000000a,0x000000000000000000000000000000000000000000000000000000000000a86a00000000000000000000000000000000000000000000000000000000000000010000000000000000000000001140cb7cafacc745771c2ea31e7b5c653c5d0b800000000000000000000000000000000000000000000000000000000000000007,0x000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000e1a3af1f9cc76a62ed31ededca291e63632e7c40000000000000000000000000000000000000000000000000000000000000004,0x000000000000000000000000000000000000000000000000000000000000a4b1000000000000000000000000000000000000000000000000000000000000000100000000000000000000000089644ca1bb8064760312ae4f03ea41b05da3637c0000000000000000000000000000000000000000000000000000000000000004,0x000000000000000000000000000000000000000000000000000000000000044000000000000000000000000000000000000000000000000000000000000000010000000000000000000000002233f8a66a728fba6e1dc95570b25360d07d55240000000000000000000000000000000000000000000000000000000000000002,0x000000000000000000000000000000000000000000000000000000000000210500000000000000000000000000000000000000000000000000000000000000010000000000000000000000002dc219e716793fb4b21548c0f009ba3af753ab010000000000000000000000000000000000000000000000000000000000000001]
- withDelegatecalls: [false,false,false,false,false,false,false]
- startBlock: 18621879
- endBlock: 18641079
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x5f8349082690bd85372f956b70ef80d8ab98f9eb6f4b8b1e1d849afadb7b51fc
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://raw.githubusercontent.com/bgd-labs/seatbelt-for-ghosts/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/375.md](https://raw.githubusercontent.com/bgd-labs/seatbelt-for-ghosts/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/375.md)

**Payloads reports**

- Ethereum

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/20.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/20.md)

- Polygon

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/10.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/10.md)

- Avalanche

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/7.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/7.md)

- Optimism

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/4.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/4.md)

- Arbitrum

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/4.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/4.md)

- Base

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/1.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/1.md)

* Seatbelt doesn't support Metis at the moment

<br>

### Technical analysis

We have verified that, per network, the following changes are applied by using the Aave BGD config engine.

**Ethereum**

[v2](https://etherscan.io/address/0x21A18A52529e252AFC26AFc4Dfb386860035e35d#code#F1#L16)

USDT

- Variable slope 1: 4% -> **5%**
- Reserve factor: 20% -> **25%**

USDC

- Variable slope 1: 4% -> **5%**
- Reserve factor: 20% -> **25%**

USDP

- Variable slope 1: 4% -> **5%**

FRAX

- Variable slope 1: 4% -> **5%**

LUSD

- Variable slope 1: 4% -> **5%**
- Reserve factor: 20% -> **25%**

SUSD

- Variable slope 1: 4% -> **5%**

GUSD

- Variable slope 1: 4% -> **5%**


<br>

[v3](https://etherscan.io/address/0x659C3e5965255A492B2923A404317A17673cb43a#code#F1#L16)


USDT

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

USDC

- Variable slope 1: 3.5% -> **5%**
- Base stable borrow rate: 4.5% -> **6%**

FRAX

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

LUSD

- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**


<br>

**Polygon**

[v2](https://polygonscan.com/address/0xCC8480b54dAc41A79B63A5D9ec3bF12b1F6BF330#code#F1#L16)

USDC

- Variable slope 1: 4% -> **5%**

DAI

- Variable slope 1: 4% -> **5%**

USDT

- Variable slope 1: 4% -> **5%**

<br>

[v3](https://polygonscan.com/address/0x7166130EB53161d17f89E8690Abc748DA3f00607#code#F1#L16)

USDC

- Variable slope 1: 3.5% -> **5%**
- Base stable borrow rate: 4.5% -> **6%**

DAI

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

MAI

- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

USDT

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

<br>

**Avalanche**

[v2](https://snowtrace.io/address/0xCDB9ea7F9443fA9e8ba6EBC9Ef41C3ed75939663#code#F1#L16)

USDC.e

- Variable slope 1: 4% -> **5%**

USDT.e

- Variable slope 1: 4% -> **5%**

DAI.e

- Variable slope 1: 4% -> **5%**

<br>

[v3](https://snowtrace.io/address/0x783719Ae64bd69F7534f3E57ccA4199f54277665#code#F1#L16)

MAI

- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

USDt

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

USDC

- Variable slope 1: 3.5% -> **5%**
- Base stable borrow rate: 4.5% -> **6%**

FRAX

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

DAI.e

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

<br>

**Optimism**

[v3](https://optimistic.etherscan.io/address/0x1EC6efd07F8f7FCceD48872E3e9043c4A7e3825D#code#F1#L16)

USDC

- Variable slope 1: 3.5% -> **5%**
- Base stable borrow rate: 4.5% -> **6%**

sUSD

- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

USDT

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

DAI

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

LUSD

- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

MAI

- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

<br>

**Arbitrum**

[v3](https://arbiscan.io/address/0x1054420C7Daf70C02a42D57D6cFe93A53cA51E74#code#F1#L16)

FRAX

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

MAI

- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

LUSD

- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

DAI

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

USDC (native)

- Variable slope 1: 3.5% -> **5%**
- Base stable borrow rate: 4.5% -> **6%**

USDT

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

USDC (bridged)

- Variable slope 1: 3.5% -> **5%**
- Base stable borrow rate: 4.5% -> **6%**

<br>

**Metis**

[v3](https://andromeda-explorer.metis.io/address/0x6c3bD2D5885D9e8a9B48c403EEb7A25195b7CCc1/contracts#address-tabs)

m.USDC

- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

m.USDT

- Optimal point: 80% -> **90%**
- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

<br>

**Base**

[v3](https://basescan.org/address/0x445a95c7e70673188417995425047bF541eEc19D#code#F1#L16)

USDbC

- Variable slope 1: 4% -> **5%**
- Base stable borrow rate: 5% -> **6%**

<br>

---

<br>


The proposal is consistent with the description on the governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.


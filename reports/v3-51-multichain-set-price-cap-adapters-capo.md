# Proposal 51. Set Price Cap Adapters (CAPO).

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=51](https://vote.onaave.com/proposal/?proposalId=51)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-correlated-asset-price-oracle/16133](https://governance.aave.com/t/bgd-correlated-asset-price-oracle/16133)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xb20935059e3F49Cbfa35bED0780Fb8887D7D0D67#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x2d976a898522e6Bca5bf1464931283d24D2A2698#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x882cCd8087bC44105E962Bc01280A335b210d738/contract/43114/code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xE2FaD8c2e3AefBB3e8FEa1E0B84463C7C06350A3#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x296C266263bDc0b4eF32F75a7769aB925772F6Cb#code#F1#L1)

* Metis - [proposal payloads](https://andromeda-explorer.metis.io/address/0xAE04aDeC3Ce3140d34377FB38C71C882E948AA03/contracts#address-tabs)

* Base - [proposal payloads](https://basescan.org/address/0x360eF8D31B90718f13b73d10f3F3C122d86577f1#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xaC603d82de4Fed4c28175f707BC4d15d79E63303#code#F1#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0x2683F613a899694a8d8669243321541CBdc6a95b#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xD11f81a205b2ae847cB46c58e12b4c82A30e1809#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade

<br>

### Context

This proposal activates the correlated-assets price oracle (CAPO) system for LSTs and fiat-pegged stable coins in order to add an upper side protection.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x078c4a41243394a23951a4826b239b7c35fb8063dd6dcd613c6ea3fec0d46e3d](https://etherscan.io/tx/0x078c4a41243394a23951a4826b239b7c35fb8063dd6dcd613c6ea3fec0d46e3d)

```
- proposalId: 51
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x79e8c356e4702464805f27c70515d01da6f5d38e3659d4ebe345aafb5b517484
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
      "payloadId": "80" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "41" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "15" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "17" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "15" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "6" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "8" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "4" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "5" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "2" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x79e8c356e4702464805f27c70515d01da6f5d38e3659d4ebe345aafb5b517484" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/51.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/51.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/80.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/80.md)

* Polygon V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/41.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/41.md)

* Avalanche V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/15.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/15.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/17.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/17.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/15.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/15.md)

* Metis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/6_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/6_forge.md)

* Base V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/8.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/8.md)

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/4.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/4.md)

* BNB V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/5.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/5.md)

* Scroll V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/2_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/2_forge.md)

<br>

### Technical analysis

We have verified that the payload changes the Asset Source of the following tokens on the following chains:

- Ethereum:

    LUSD: 0x9ecdfacca946614cc32af63f3dbe50959244f3af

    DAI: 0xaeb897e1dc6bbdced3b9d551c71a8cf172f27ac4

    PYUSD: 0x150bae7ce224555d39afdbc6cb4b8204e594e022

    wstETH: 0xb4ab0c94159bc2d8c133946e7241368fc2f2a010

    FRAX: 0x45d270263bbee500cf8adcf2abc0ac227097b036

    USDC: 0x736bf902680e68989886e9807cd7db4b3e015d3c

    rETH: 0x5ae8365d0a30d67145f0c55a08760c250559db64

    cbETH: 0x6243d2f41b4ec944f731f647589e28d9745a2674

    USDT: 0xc26d4a1c46d884cff6de9800b6ae7a8cf48b4ff8

    crvUSD: 0x02aee5b225366302339748951e1a924617b8814f

- Polygon:

    wstETH: 0xbd96b5abbc6048c28184b462167e487533f2e35e

    USDC: 0x17e33d122fc34c7ad8fbd4a1995dff9c8ae675eb

    stMATIC: 0x6d02e35031c4d99ee3a6a2ba47fad0cfe355ca8f

    USDC.e: 0x17e33d122fc34c7ad8fbd4a1995dff9c8ae675eb

    DAI: 0xf86577e7d27ed35b85a7645c58baaa64453fe32b

    miMATIC: 0x4ae2ab1af7e3b0092dbf3a4b20ec3de8fc834873

    USDT: 0xaa574f4f6e124e77a7a1b5ed91c8b407000a7730

    MaticX: 0xb0a72a5e454890e9715e059e8df8582a6b383de3

- Avalanche:

    sAVAX: 0xb2b332f27e4b7305649a228c31ed9858c5a6bad9

    MAI: 0xccc55db26b78a19dba1bee0066f9c1665575439a

    USDt: 0x39185f2236a6022b682e8bb93c040d125da093cf

    USDC: 0xd8277249e871be9a402fa286c2c5ec16046dc512

    FRAX: 0x6208576378d06ce69a27987b7a524a9b15d499a4

    DAIe: 0xf82da795727633afa9bb0f1b08a87c0f6a38723f

- Optimism:

    USDC.e: 0x2daa7078f78485a708003989cbc9a643e3b4b61f

    wstETH: 0x724e47194d97263ccb71fdad84b4fed18a8be387

    USDC: 0x2daa7078f78485a708003989cbc9a643e3b4b61f

    sUSD: 0xc77e9cf9603f5ef5503213229abb1fec3001f312

    USDT: 0x70e6dbbffc9c3c6fb4a9c349e3101b7dcee67f4d

    rETH: 0xf17e75d58d4be71b8e674fa104b71a827e38f087

    LUSD: 0x8f4dafb6feb190e7846eb7665fd49ffb1177ff8e

    DAI: 0x1a96fe91278bcf6f19665f642fe7a88cd5c360bb

    MAI: 0xc6ac65e8f4f50a6655efd78a92b6c503b5b625c8

- Arbitrum:

    FRAX: 0x06919eb75bd6ba817d38cc70c1ca588ac7a01c10

    MAI: 0x7a7ce08a1057723ccedea2462407427ae33ffeb2

    wstETH: 0x87fe1503befbf98c35c7526b0c488d950f822c0f

    LUSD: 0x341b110bdf665a20f0d5f84a92fcaf5ebeebc629

    USDC.e: 0xde25a88f87fed9f8999fabf6729dcb121893623c

    DAI: 0x4a838a3dac6633bb1fd932b6f356decfcaf7803d

    rETH: 0x256f33fc0110b1297f78f48524631d30b752480d

    USDT: 0x84dc1c52d7c340aa54b4e8799fbb31c3d28e67ad

    USDC: 0xde25a88f87fed9f8999fabf6729dcb121893623c

- Metis:

    mDAI: 0xB3721282cd62Ba8F7bB02Cb843F3a34f9e109ef8

    mUSDC: 0xF2acD6aE4fcf662161eA354dA844f224bf91FF8c

    mUSDT: 0xD1D7DCBDE72916646A7F8AcE6Ad8C5179D8ddFbB

- Base:

    cbETH: 0x8e11ad4531826ff47bd8157a2c705f5422da6a61

    USDC: 0x978d8878b53fbe40dab7d4ab47b97ab622ffef9f

    wstETH: 0x56038d3998c42db18ba3b821bd1ebab9b678e657

    USDbC: 0x978d8878b53fbe40dab7d4ab47b97ab622ffef9f

- Gnosis:

    wstETH: 0x8ee42ba520ca106294163fb8b1ffe9c6fba35507

    USDC: 0x0a2d05bc646c65a029e602c257dfa14adf8bfad2

    WXDAI: 0xe5269ef0ce04e509e8134624c7bf043b21e10897

- BNB:

    USDT: 0x0f682319ed4a240b7a2599a48c965049515d9bc3

    USDC: 0xafcff74ae956f4c23c27db49659d4a7f350415c1

    FDUSD: 0x60a117fa5babee4d645884fb11e413da4f893b6d

- Scroll:

    USDC: 0x427Fd98dbD1DbC2D4e792350caBe7c9665F35bee

    wstETH: 0x4EdAbf45e78363b8Dcd763bBbd05665c6e24975C

<br>

The proposal is consistent with the description on the governance forum except sDAI which has been postpone and EURe which is not possible to implement at the moment as the price feed needed is missing.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

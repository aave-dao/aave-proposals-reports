# List Of Checks Done

## proposal 2:
- on V2:
    - We checked that the (correct) asset was forzen
    - We checked that the values that were declared to be updated in the proposal were indeed adjusted to on the correct asset and to the declared values
    - We checked that no other parameters were changed on this proposal
    - We checked that the changes were applied on the correct market (v2 and not v3 for example)

- on V3:
    - We checked that the (correct) asset was forzen
    - We checked that the values that were declared to be updated in the proposal were indeed adjusted to on the correct asset and to the declared values
    - We checked that no other parameters were changed on this proposal
    - We checked that the changes were applied on the correct market (v3 and not v2 for example)

- What we didnt check:
    - Create2 of real addresses
    - e2e tests and additional tests made by the proposer


## proposal 3:
- For each market:
    - checkd that the correct market was called (Ethereum V2 or V3, etc, depending on the payload)
    - We checked that the values that were declared to be updated in the proposal were indeed adjusted to on the correct asset and to the declared values, i.e. slope 1 was changed to 6% (6_00) 
    - We checked that no other parameters were changed on this proposal, i.e. all other values were kept the same


## Questions:
- On avalanche (and other chains) how can we know that the assets being updated are the ones intended? the ipfs states for example usdc but the implementation refers to usdc.e. How can we know that is what intended?
- Seatbelt of metis is broken link, what should be done?


## Findings:
1.  Dai on ethV2 is not stated on snapshot, but is on ipfs + code - the forum discussion states clearly that some assets were added after the snapshot
2.  same in ethV3 - the forum discussion states clearly that some assets were added after the snapshot
3.  Arbitrum V3 on snapshot claims that USDC.e is 5%, but on IPFS it claims that it’s 7% - going to the IR strategy it is indeed 7% so no action should be made 
4.  Gnosis is not at all included in the snapshot - the forum discussion states clearly that some assets were added after the snapshot


## Verdict:
No issues were found
# Extract weekly rewards from UBE-CELO pool -> 

We aim to compare the values displayed in the UI (https://app.ubeswap.org/#/farm) with values obtained from CELO`s smart contracts, whereas the latter can be automated and fetched automatically.

**Note the global variable:**
```
number_of_seconds_in_week = 7 * 24 * 3600
```

I did the following manual steps:

- Get CELO weekly rewards (Concept OK, Implementation not done)

    - Moola Staking rewards https://explorer.celo.org/address/0x9D87c01672A7D02b2Dc0D0eB7A145C7e13793c3B/read-contract
    
    (see vfat.tools/celo_ube.js for pool addresses)

    - Divide rewardRate / 1e18 * number_of_seconds_in_week = number of Celo per week


- Get UBE weekly rewards (Concept OK, Implementation not done)

- CELO-UBE liquidity pool (address obtained from vfat.tools) https://explorer.celo.org/address/0x295D6f96081fEB1569d9Ce005F7f2710042ec6a1/read-contract
    
    - Divide rewardRate / 1e18 * number_of_seconds_in_week = number of UBE per week


Not implemented
- Automatic retrieval of APY per code (basically dividing reward rates in USD by total value locked and add compounding semi-annually - like Ubeswap displays in the tooltip)
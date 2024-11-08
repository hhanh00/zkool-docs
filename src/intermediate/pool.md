# Pools

Zcash is basically three cryptocurrencies in one. Logically,
we could talk about transparent ZEC, sapling ZEC, and orchard
ZEC. But because there is a 1 for 1 ZEC exchange rate between
these, we simply say ZEC.

The protocol deals with ZEC in 3[^1] very different ways.

> Zcash has three pools of ZEC: Transparent, Sapling & Orchard.

Transactions can include any pool as both inputs and outputs.
They can use multiple pools too.

## Transparent Pool

- Based on the Bitcoin protocol, it offers **no privacy**. Transactions
are in clear. Addresses and amounts are public.
- Synchronization is **very fast**[^2] because the wallet app
communicates with servers that have indexed the Blockchain

## Sapling Pool

- Second version of the Shielded Protocol, it offers **full privacy**.
Transactions are encrypted. Addresses and amounts are hidden.
- Transaction graph is hidden[^3]
- Synchronization is slow. The wallet app has to download and
try to decrypt every transaction[^4]
- There is a **trusted setup**. Users must trust that the creation
of the blockchain was done honestly[^5]
- Any change in the protocol requires a new trusted setup
- Proofs are short, quick to create and verify

## Orchard Pool

- Third version of the Shielded Protocol, it offers **full privacy**.
Transactions are encrypted. Addresses and amounts are hidden.
- Transaction graph is hidden[^3]
- Synchronization is slow. The wallet app has to download and
try to decrypt every transaction[^4]
- There is no trusted setup
- Proofs are longer, slower to create and verify (than Sapling)
- The system has room for further cryptographic improvements[^6]

```admonish warning
Using the right pool is paramount to your privacy. However
not every app/business support every pool. You may have
to move funds between pools.

Be careful when you use the transparent pool as it offers
no privacy at all.
```

## Pool Transfers

![Pool Transfer]({{rootUrl}}/images/2024-11-07_13-32-28.png "pool" =450x)

The Pool Transfer page offers a convenient way to move/accumulate
funds to a pool[^7].

1. This is the current distribution of funds across the pools
1. Summary of your available funds. Refer to 
[Funds](../basic/send.md#funds) for more info
1. Pools from and to selection. You can select multiple source
pools but only one destination pool
1. Amount
1. Memo
1. When you specify a non-zero amount, the output is split
into several notes if the amount exceeds the "Max per note"

> We recommend having several notes for better
flexibility in your spending.

Having a few notes helps make several transactions concurrently.
Notes cannot be partially spent; therefore, you need to wait for the
change to come back and for it to mature. 
In the meantime, you can use another note if you have several of them.

Zkool/Ywallet does not automatically move funds between pools.
At the moment, the ecosystem does not have a dominant
pool and each pool has pros and cons.

> We believe the user should be in charge of their wallet
and how they distribute their funds between the different pool.

---
[^1]: Technically, 4 ways because there is also Sprout. But
Sprout is now deprecated. It is only possible to spend
from it.
[^2]: Less than 1 second per address.
[^3]: Not merely obfuscated.
[^4]: By providing a birthday height, the wallet app can
skip the blocks prior to the account creation. This can
save a lot of time.
[^5]: To mitigate this issue, the creation was a cooperative
event involving hundreds of participants. The protocol is
secure as long as a *single* participant was honest.
[^6]: Batch verification and recursive proofs are a few of these.
[^7]: You can achieve the same results by executing a transaction
to your own account, but the pool page has a few more capabilities.

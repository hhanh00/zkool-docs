# Transparent Wallet

The Zcash ecosystem has two types of wallets: Transparent and Shielded wallets.

Transparent wallets do not support shielded transactions at all. They offer some
privacy by generating new addresses whenever they detect usage of the current
address.

Shielded wallets embrace the sapling and orchard protocol. However, their
support of transparent transactions is less feature-rich. They rely on the user
moving their funds to the shielded pools as soon as possible.

That's a fair assumption most of the time, but *the long synchronization time
deters many users*. They either continue using a transparent wallet or migrate to
a shielded wallet while leaving their funds in the transparent pool.

Neither approach is optimal. 

```admonish warning
The longer someone uses a transparent wallet, the
longer their privacy is at risk. The Transparent pool is as public as Bitcoin.
*Their privacy is even worse if they move to a shielded wallet but leave their
funds in the transparent pool*.
```

At least a transparent wallet does not reuse
addresses[^1].

Zkool is primarily a shielded wallet app, and we encourage users to leverage the 
shielded pools for their bulletproof privacy feature.

Yet, we also know that many of our potential users would prefer to keep at least a 
portion of their funds in the transparent pool.

That is why Zkool rotates its transparent addresses. Due to limitations in the
light wallet protocol, using multiple transparent addresses is slower than it
should be[^2].

> As a result, you may notice your main address change when you receive funds in 
your transparent address.

Zkool will derive a new set of transparent keys and align the diversified shielded 
addresses with them—consequently, the account unified address changes.

You can manually derive new transparent address or switch back to an old
address using the Transparent Address menu in the More tab.

---
[^1]: A few shielded wallet apps automatically move the funds to the shielded pool.
However, we don't like this option because it would be as if a financial
institution automatically moves their customer's funds.
[^2]: We hope that the protocol will be upgraded in the future.

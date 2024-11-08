# Address Diversification

When an account gets created, it has one set of keys: one
transparent, one sapling and one orchard key[^1].
Therefore, the account has one set of receivers and
one Unified Address that include all receivers.

But sometimes, that is not enough.

Shielded addresses do not appear on the Blockchain. But
if you give your address to different people, they
obviously can link to your identity if they cross-reference
it.

This can be prevented if you give distinct addresses to
every payer.

> Address diversification is the ability to have multiple
addresses in the same account.

The Transparent and the Shielded protocols both have
address diversification, but the implementation works
differently.

## Transparent Address Diversification

We can derive many *lists* of addresses from a single
seed phrase using the algorithm described in BIP-32[^2].

To get a new address, the wallet app derives a new pair
of keys (secret & public). Even though they come from
the same seed phrase, they appear unrelated[^3].

The wallet app generates them following an increasing sequence
of indices.

However, if you need to restore your seed phrase in another
wallet app, the latter does not know what indices were used
to derive the addresses that you handed out. It uses a simple
heuristic[^4]: Starting from the first index, it derives
the address and checks out if that address was used in a
transaction. If so, it is *not* the last address and the wallet
app goes to the next index.
When there are many[^5] consecutive unused addresses, the
wallet app considers that it reached the end.

This method assumes that the address indices were used in increasing
order without large gaps.

```admonish warning
When you move your account to a new installation, there is no
firm guarantee that transparent addresses are not reused.
```

An address could have been given to a payer, but he has not used
it yet. The wallet that recovers from seed phrase does not know
which index was last used.

## Shielded Address Diversification

The good news is that address diversification is built in
the protocol. You can derive many addresses from a single
secret key, whereas the transparent protocol only allows one
address per secret key.

Even better, scanning diversified shielded addresses does not
take additional time.

The wallet app tries to decrypt every shielded transaction output
to look for its notes[^6] using the *incoming viewing key*.

> Every diversified shielded address has the same incoming
viewing key.
The wallet app does not need to try every *shielded diversified
address*, just the key.

```admonish note
Diversified Shielded Addresses are not supported by many wallets.
Unfortunately, early shielded wallets were using the same
logic as Transparent addresses, leading to unacceptable
performance[^7] when the Blockchain increased in size.
```

If you need shielded address diversification, make sure that
your wallet app uses the right technology.

---
[^1]: Assuming that the user created the account from a seed
phrase.
[^2]: BIP are documents that specify improvements to the
protocol.
[^3]: There is no way to tell that two secret keys come
from the same seed phrase without knowing the seed phrase
and the index of the keys.
[^4]: Basically, it tries out and hopes for the best.
[^5]: It stops after a certain gap is reached.
That value is called the gap limit.
[^6]: This is like having a key and a hundred million doors.
Trying to open each door takes a while.
[^7]: The wallet app could not handle the load and crashed.
User funds were stuck. It was bad.

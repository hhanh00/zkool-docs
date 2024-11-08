# Keys

In Zcash, every account has several keys.
In fact, it has many keys, more than a dozen.
Fortunately, most of them are used internally
by the protocol, and we do not need to know
about them. But, this still leaves a good number
of keys that we *may* need to use.

> Every key is derived[^1] from the seed phrase.
If you do not have to import/export your account
to another wallet app that does not support
seed phrases, then the seed phrase is the *only*
key that you must save.

Again, all the keys besides the seed phrase are
for interoperability with other wallet apps.

That disclaimer being said, here are the keys
that an account has:

![Keys]({{rootUrl}}/images/2024-11-07_22-20-46.png "keys" =450x)

1. Sapling secret key
1. Unified viewing key
1. Sapling viewing key
1. Extended transparent secret key
1. Transparent secret key
1. Extended transparent public key
1. Transparent address (not really a key, but it gives access
to the transaction history)

The first 3 keys are shielded (sapling/orchard) keys and the
remaining are transparent keys.

## Key Capabilities

- A key can allow you to spend funds (that's a *secret* key),
or view funds but not spend them (that's a *viewing* key).
- A key can also allow you to derive[^1] more keys (and addresses).
The section on [Address Diversification](div_address.md)
explains why this is often desirable.

These two capabilities are orthogonal. For example, a key can allow
you to derive more viewing keys but not secret keys.

In the next section, when we describe a key, we will indicate what
its capabilities are.

## Shielded Keys

### Sapling secret key
The sapling secret key is an old type of keys. It comes
from `zcashd` before it supported seed phrases. A
sapling secret key begins with `secret-extended-key`.
It can sign sapling transactions but neither transparent
nor orchard transactions.
### Sapling viewing key
The sapling viewing key is an old type of keys. It comes
from `zcashd` before it supported seed phrases. A
sapling secret key begins with `zxview`.
It can decode an address sapling transaction history but
cannot see the transparent and orchard history.
### Unified viewing key
The Unified viewing key is the viewing key equivalent
of a unified address. It combines several viewing keys[^2]
and depending on the included receivers, can
fully or partially decode an account transaction history.

## Transparent Keys

- Keys that can derive additional keys are called Extended Keys
- We have secret and public keys

There are 4 keys in total: Extended secret key, extended public key,
secret key and public key.

Since transparent transactions are public, the address
serves as the viewing key[^3].

---
[^1]: Derivation is a one way street. When A derives
B, we can compute B if we know A, but we cannot
compute A if we know B.
[^2]: There are 7 possible combinations of receivers
(T, S, O, T+S, T+O, S+O, and T+S+O).
[^3]: Technically, there is a public key too. But the address
is all that is needed to view the transactions.

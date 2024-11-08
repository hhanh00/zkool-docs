# Addresses

![Home Page]({{rootUrl}}/images/2024-11-06_21-53-23.png "home" =450x)

It used to be possible to recognize a pool by address.
For instance, an address that begins with a `t` is
a transparent address from the transparent pool.

Likewise, an address starting in `zs` would be from
the sapling pool.

But starting from the orchard pool, there is no longer
a unique, distinguishable address format.

Orchard addresses begin with `u` but all u-addresses
are not necessarily orchard.

Instead, u-addresses (called Unified Addresses) contain
one or many[^1] *receivers*. A receiver is the generic
term for (what used to be) an address.

For example, you can have a UA with a transparent and
a sapling receiver. It is equivalent to the combination
of a `t` address and a `zs` address.

Or you can have a UA with only an orchard receiver.

> UA are designed to hide the implementation of the
protocol from the user to let the wallet app decide
what is best.

However, there aren't supported everywhere.

In Zkool/Ywallet, you can switch between address types
by swiping the QR code left/right. Your account
accepts any of these addresses. By default, you should
use the UA.

---
[^1]: up to 3, one of each pool.

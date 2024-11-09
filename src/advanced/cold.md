# Cold Storage

> Cold Storage is the storage of funds in a wallet app that stays *always*
disconnected from the Internet.

The key word is *always*. It is not sufficient to occasionally turn off the
network access from a wallet to make it *cold*.

```admonish warning
Cryptocurrency wallets are a prime target for malware. They can infect your
computer/phone and stay dormant until you use your wallet. When they activate,
they will exfiltrate your secret keys to the hacker's computer, and your funds
are irreversibly lost.
```

Cold wallets offer the highest level of security by always keeping your precious
secret keys disconnected from the Internet.

They work by splitting the process of building a transaction into two
components[^1].

The first component stays online and gathers the data necessary to create the
transaction. However, it does not have the secret keys to sign the inputs.
Instead, it makes a data file (or QR codes) that the account owner transfers to
the second component.

> By making a manual transfer with no programmability, you can be
sure that no malware can affect the second component.

The second component, the transaction signer, stays offline at all times. It
signs the partial transaction (after validation and confirmation from the account
owner) and produces the complete transaction.

Then, the latter is transferred back to the first component for broadcast to the
network.

## Partial Transaction

The Partial unsigned transaction is created from the
transaction summary page just before you submit it
to the network[^2].

![Cold]({{rootUrl}}/images/2024-11-09_15-48-13.png "cold" =450x)

## Sign and Broadcast

This is performed through the Sign and Broadcast menus
in the More Tab.

Use "Sign" on the offline device and "Broadcast"
on the online device.

## Watchonly account

You should never have the secret key or seed phrase
of a cold wallet on an online device.

To setup a cold wallet, you need to start
on the offline device (the signing device).

1. Create a new account.
1. **Save the seed phrase in a secure place in case
you lose access to the signer**.
1. Display the unified viewing key UVK
1. Import a new account on the online device
by scanning the UVK

---
[^1]: Or more components, if it involves multiple signatures.
[^2]: In the image, the account also has the secret key.
In reality, the online wallet should only have the
*viewing key*.

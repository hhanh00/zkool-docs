# Create New or Restore Old Accounts

![New]({{rootUrl}}/images/2024-11-06_22-08-18.png "home" =450x)

1. Name of the Account. Required but does not have to be unique
1. Toggle between new account and import account
1. Seed phrase or a secret/viewing/public key[^1]
1. Toggle if you don't want to have shielded addresses in this account[^2]
1. Account derivation index. This should be left unchanged unless you
want to have several accounts with the same seed phrase
1. Account *birth height*. Height at which this account was created.
Defaults to the current height

```admonish warning
You almost certainly want to enter a birth height otherwise
synchronization will download and scan the blockchain from the
start (and take **hours**).
```

---
[^1]: See [Keys](../advanced/keys.md) for the supported key types
[^2]: Some exchanges prohibit using shielded addresses

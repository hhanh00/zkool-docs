# What's new?

## Accounts
The account system has be rebuilt. Accounts have
independent transparent, sapling and orchard keys.
There is no need of a sapling key and
secret transparent keys can be imported[^1].

Users can have distinct accounts based on
the kind of usage. For instance, a transparent
only account works well with Binance as it
requires sending funds from a transparent address.

## Unified Address Diversification

Ywallet keeps a single address per pool.
Sapling and orchard diversified addresses are
based on the current time[^2].

Zkool has these diversified addresses too,
and adds diversified unified addresses based on
an incremental number. It allows them to
include a transparent receiver.

## Unique Transparent Address

Whenever Zkool detects that one of its transparent
addresses is used, it will automatically generate
a new fresh one. Transparent accounts do not
reuse the same address as most shielded wallets do.

## Enhanced Transaction Details

The transaction details page has all the inputs
and outputs. Ywallet only shows a detailed summary.

## Synchronization

> ZKool uses Warp2 whereas Ywallet is on Warp.

- Warp2 leverages a server that gives pre-filtered blocks[^3].
- On desktop, Zkool can download a bootstrap
blockchain file[^4].
- Warp2 can use regular lightwalletd servers but then, it is without
spam filtering.

## Keys

We now support all types of unified viewing keys and
extended transparent keys.

## Payment URI

Payment URI supports multiple recipients. You can
store a multi-pay transaction as a Payment URI
for later use or reuse.

## Minor Improvements

- Pool Transfer can use multiple pools as source
- Unconfirmed transactions are shown in the transaction history
- Unconfirmed funds are shown on the main page
- Synchronization is more reliable when the app resumes from sleep

---
[^1]: Sweeping used to be the only way to use
a transparent secret key.
[^2]: Like TOTP (Time Based One-Time Password).
[^3]: Skipping over large transactions (indicative of Spam)
[^4]: that contains data up to block #2400000.

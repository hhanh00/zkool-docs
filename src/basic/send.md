# Send Funds

![Send]({{rootUrl}}/images/2024-11-06_22-29-35.png "home" =450x)

> The Send Page can have a lot of options. You can configure
which options to show in the settings.

By default, it displays the most commonly used options (much less than here).
Below is the *full* set of options.

1. 
    - Left Button: Toggle between simplified and *custom* send mode
    - **Send Transaction** Button
1. Address of the recipient
1. Buttons to get the address as
    - QR code (via scanner)
    - contact from the address book
    - one of the other accounts
1. Your available funds (see next section)
1. The pools that you want to use to send from and where to
1. The amount in ZEC, FIAT or as a % of the total balance (slider)
1. Toggle between 
    - sender pays the transaction fees and the recipient gets the full amount specified
    - or recipient pays the transaction fees and receives less than the amount specified
1. Sets the amount to MAX, and make the recipient pay the fees[^1]
1. If using a memo, toggle whether you want **your** address to be included[^2]
1. Memo subject & body

> The send button is on the app bar.

## Funds

- Funds that you send out are "rounded" according to the notes
available in your wallet. For instance, if you have a 10 ZEC note
and you spend 4 ZEC, your account will be debited of 10 ZEC
momentarily. Eventually, the change (6 ZEC) comes back. Then,
you need to wait for it to *mature* before it can be spent.

Section 4 shows the breakdown of your funds in several parts:
- Total funds is how much you have (not counting incoming funds)
- Unconfirmed are the funds that are in transit. They were
sent to the network but not included in a block, yet
- Immature are the funds you got confirmed, but they don't have
enough confirmations[^3]
- Spendable is what you can use right now

---
[^1]: Otherwise there would not be enough funds
[^2]: By default, memos are anonymous
[^3]: You can adjust the number of confirmations required in the settings.
This is a user preference that has a small effect on privacy and
safety in case of a rollback.

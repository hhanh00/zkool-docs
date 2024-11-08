# Notes/UTXO

Notes are the cornerstone of the system.

Every payment made through Zcash is in the form of a
transaction and transactions create and delete[^1]
notes/utxo.

> An account is just a collection of notes that you own[^2].

- Each note has an *address* and an *amount*
- An account usually has more than one note
- An account may use more than one address[^3]
- Notes refer to notes in a Shielded Protocol
- UTXO refer to notes in the Transparent Protocol[^4]

You can see what notes your account contains with the
Notes and UTXO pages.

1. Height/Number of Confirmations
1. Amount. Larger amounts are in bold face
1. Date/Time

You can exclude some notes from being used in transactions
by selecting them. 

> Highlighted notes will not be spent.

![Notes]({{rootUrl}}/images/2024-11-07_12-32-53.png "notes" =450x)

---
[^1]: Blockchains are permanent. Therefore, nothing
is physically deleted. However, notes are logically
deleted by creating an entry that marks a previous
note as used/spent.
[^2]: Owning a note means having the secret key that
allows to sign a transaction that spends the note.
[^3]: For more info, see the section on
[Address Diversification](../advanced/div_address.md).
[^4]: The term UTXO comes from the original Bitcoin paper

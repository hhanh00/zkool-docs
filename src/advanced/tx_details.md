# Transaction Details

On top of the usual txid, height, address, amount, etc
the transaction history page display a detailed view
of the inputs & outputs. Some block explorers
offer a similar view[^1] but Zcash encrypts shielded inputs/outputs.

> The Transaction Details shows every input and output,
including the shielded ones as long as they can be decrypted.

![Transaction Details]({{rootUrl}}/images/2024-11-09_12-22-05.png "tx_details" =450x)

1. Indicates the direction
    - left arrow, input
    - right arrow, output
1. Address if it can be decrypted. Otherwise the name of the pool
1. Amount if it can be decrypted. Otherwise '?'

The details are given from the point of view of the transaction,
and not from the account.

Inputs (left arrows) are funds
that enter the transaction. Hence, they represent funds
that are *spent* from the account.

Outputs are funds that exit the transaction. These funds
can either go to your account, i.e. they are funds that
you *receive*[^2] or that you sent to another user.

---
[^1]: For bitcoin, here is an [example transaction](https://www.blockchain.com/explorer/transactions/btc/cb9b39beb438cf42830fc85653a6d2b764cea11a709ce22b53b9ff1d3264a730).
[^2]: It could be the change too.

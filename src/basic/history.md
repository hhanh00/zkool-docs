# Transaction History

![History]({{rootUrl}}/images/2024-11-06_23-18-21.png "home" =450x)

1. Initial of the sender or recipient (when known[^1])
1. Address and message
1. Date/Time and amount

```admonish tip
You can switch to a table display by switching to
landscape mode (by rotating your device/phone, or by resizing
the window)[^2].
```

## Transaction Details

Tapping on a transaction will show you its details.
The information is detailed in the section
[Transaction Details](../advanced/tx_details.md).
The main fields are the following:
- TXID, the transaction ID
- Timestamp
- Amount
- Number of Confirmations: How many blocks are after the one
that included the transaction[^3]
- Memo/Message

## Messages

Memos are gathered in a dedicated tab for easier navigation.

---
[^1]: The source of the funds may be hidden. 
When the funds come from a shielded address, the protocol
hides it from the recipient. Also, it is possible to send to a
shielded address and then "forget" about it. It is rare but allowed
by the protocol.
[^2]: You can also manually change it in the settings.
[^3]: +1 since the block that includes the transaction counts as 1.

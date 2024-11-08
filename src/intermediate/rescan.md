# Rescan

The wallet app synchronizes automatically during normal
operations. There is no need to do anything.

However, if you restore old accounts that have
transactions in the past, you have to rescan or rewind
for the wallet app to see these transactions.

Rescanning *deletes all the synchronization data*,
then redownloads and reprocesses the blockchain from the
given block height. You cannot rescan a single account;
therefore the rescan should start from the lowest block
height of your accounts[^1].

If you want to restore multiple accounts, it is highly
recommended to first recreate all the accounts and then
perform a single rescan.

> All accounts are rescanned together.

Rescan is also useful when you notice something odd with
your wallet data and want to fix it without having to
reinstall the app, and recreate accounts. This is
a "factory reset" that preserves your account keys.

## Rewind

Alternatively, you can rewind the synchronization data
to a previous checkpoint.

Rewinding does not delete your synchronization data.
Instead, it restores it to a previous block height and proceeds
to redownload and reprocess from that point.

It is preferred over rescanning because it partially
preserves previous synchronization data, and you do not
need to scan as much Blockchain data again.

> Zkool/Ywallet uses the WarpSync algorithm that skips over
blocks. You can only rewind to one of the "checkpoints[^2]".

This implies you cannot rewind to a height lower than you started
the last rescan.

---
[^1]: The app chooses that height by default.
[^2]: Checkpoints are created at the end of a synchronization phase.
If you keep your wallet closed, there won't be any checkpoint for
that period.

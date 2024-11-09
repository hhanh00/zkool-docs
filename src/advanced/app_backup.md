# App Backup

The Wallet App backup is an encrypted database archive of all
the app data.

That includes accounts, contacts, and synchronization data.

App backups are compatible between devices and platforms. You
can import your accounts on a powerful desktop computer,
synchronize and transfer the app backup to your phone.

This way, all of your data gets copied in seconds.

However, app backups are not interoperable with other
wallets[^1].

> App backups are not a substitute for saving the
seed phrase.

To use them, you need to have an encryption/decryption
keypair[^2].

![App Backup]({{rootUrl}}/images/2024-11-09_15-58-23.png "app_backup" =450x)

- The encryption key (starting with `age`) is for making a backup.
- The decryption key (starting with `AGE-SECRET-KEY`) is for
restoring the backup. They work as a pair. One is useless
without the other[^3].

The app backup can be stored on the cloud because it uses
strong encryption.

---
[^1]: Including between Ywallet and Zkool.
[^2]: This is not the same key as Zcash uses.
[^3]: The encryption key can be recomputed from the decryption key,
but we strongly recommend you keep them both.

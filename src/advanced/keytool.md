# Key Derivation

## Transparent Derivation
![Key Derivation]({{rootUrl}}/images/2024-11-10_00-17-31.png "keyd" =450x)

Derivation for Transparent addresses use BIP 32 and the path
`m/44'/133'/account'/external/index`

For example, for the account #2, the change address at index #5
is `m/44'/133'/2'/1/5`.

1. Click to expand
1. Toggle between Transparent and Sapling

## Sapling Derivation
![Key Derivation]({{rootUrl}}/images/2024-11-10_00-17-56.png "keyd" =450x)

Orchard keys are also derived from the seed phrase, but they cannot
be individually exported, and they are not shown in the keytool.

1. Click to expand
1. Note that some indices are N/A. Sapling derivation does not
cover every index[^1].

---
[^1]: Transparent and orchard indices are also *skipped* in
alignment with sapling. Otherwise, the unified address could
contain receivers that use different indices. 
## Generating Keys, Addresses from Mnemonic

```dart
const mnemonic = ['elder', 'quality', 'this', ...];

// these should never be stored in memory, only in encrypted storage if at all
final masterKeyPair = MasterKeyPair.fromMnemonic(mnemonic);

// generate keys, addresses, puzzlehashes at desired derivation index (both hardened and unhardened)
final walletKeyAddressSet = WalletSet.fromPrivateKey(masterKeyPair.masterPrivateKey, 0);
```

## Run Wallet Demo Test
```console
Irulast-MacBook-Pro:chia-crypto-utils irulastdev$ run test/utils_test/utils_test.dart

00:00 +0: should generate correct puzzle hashes from mnemonic

Fingerprint: 3109357790
Master public key (m): 901acd53bf61a63120f15442baf0f2a656267b08ba42c511b9bb543e31c32a9b49a0e0aa5e897bc81878d703fcd889f3
Farmer public key (m/12381/8444/0/0): 8351d5afd1ab40bf37565d25600c9b147dcda344e19d413b2c468316d1efd312f61a1eca02a74f8d5f0d6e79911c23ca
Pool public key (m/12381/8444/1/0: 926c9b71f4cfc3f8a595fc77d7edc509e2f426704489eaba6f86728bc391c628c402e00190ba3617931649d8c53b5520
First wallet address: txch1v8vergyvwugwv0tmxwnmeecuxh3tat5jaskkunnn79zjz0muds0qlg2szv

00:04 +1: All tests passed!
```

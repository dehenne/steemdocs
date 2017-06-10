# WIF - Wallet Import Format

WIF is a Base58 format for private ECDSA keys for easier storing/copying. The acronym `wif` is used in many steem libs as a parameter name for a key.

More technical documentation [here](https://en.bitcoin.it/wiki/Wallet_import_format).

### Steem supports 4 different keys for the interaction with the network:

Owner: Thats the master key to control everything for a user. It can change all other keys including itself.

Active: Transaction key for spending Steem, powering up/down etc. Cannot change owner key.

Posting: Social actions, only for posting and curation.

Memo: Encrypt and decrypt private messages/memos e.g. in transactions.


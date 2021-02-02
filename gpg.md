# GPG Cheatsheet

Use [this](https://www.devdungeon.com/content/gpg-tutorial) as reference.

```shell
# LIST KEYS
gpg --list-keys  # public
gpg --list-secret-keys  # private

# CREATE NEW PRIVATE KEY
gpg --gen-key

# EXPORT PRIVATE KEY
gpg --export-secret-keys --armor [ID] > ./[fname].asc

# IMPORT KEY
gpg --import ./[fname].asc

# ENCRYPT FOR A SINGLE RECIPENT (opt: --sign)
gpg --armor --recipient [ID|Email] --encrypt message.txt

# Decrypt message
gpg --decrypt message.txt.asc > decrypted_message.txt
```

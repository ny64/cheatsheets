# GPG Cheatsheet

## Key management

### List keys
##### Public
<code>gpg --list-keys</code>
##### Private
<code>gpg --list-secret-keys</code>

### Generate new key
<code>gpg --gen-key</code>

### Export private key
<code>gpg --export-secret-keys --armor [ID] > ./[fname].asc</code>

### Delete key
##### Public
<code>gpg --delete-keys [ID]</code>
##### Private
<code>gpg --delete-secret-keys [ID]</code>

### Import key
##### From file (works with both public and private)
<code>gpg --import ./[fname].asc</code>
##### From server (example)
<code>gpg --keyserver pgp.mit.edu  --recv C104CDF0EDA54C82</code>

## Encryption

### With passphrase (symmetric)
#### Prompts you for a passphrase
Creates message.txt.gpg (binary)<br>
<code>gpg -symmetric message.txt</code>
#### Same, but ASCII format output instead of binary
Creates message.txt.asc (ASCII)<br>
<code>gpg --armor --symmetric message.txt</code>
#### Specify the encryption algorithm
<code>gpg --symmetric --cipher-algo AES256</code>
#### Get the list of cipher algorithms
E.g. 3DES, BLOWFISH, AES256, TWOFISH<br>
<code>gpg --version</code>
#### Specify output file
<code>gpg --output message.txt.gpg --symmeteric message.txt</code>
Encrypt and sign (all in the single output file)<br>
<code>gpg --sign --symmetric message.txt</code>



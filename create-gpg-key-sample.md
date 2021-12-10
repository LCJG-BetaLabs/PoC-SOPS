```
$ gpg --full-generate-key

Kind of key : (1) RSA and RSA (default)
keysize: 3072
Key is valid for? : 0 (Do not expire)

Real name: <name>
Email: <email>
Comment: (blank)

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? o

Enter Passphrase 2 times (cannot be blank)

public and secret key created and signed.

pub   rsa3072 2020-11-26 [SC]
      3F73E4821B848420CDEAEAD585E2DE2374D6377A  ---> Note this value
uid                      test1 <test1@test2.com>
sub   rsa3072 2020-11-26 [E]

# Remove the passphrase if wanted
# This is important for the passphrase screen to show up in console
$ export GPG_TTY=$(tty)
$ gpg --edit-key 3F73E4821B848420CDEAEAD585E2DE2374D6377A
gpg> passwd
# 1. Type current passphrase
# 2. Type "" (Blank)
# 3. Type "" (Confirm Blank)
```

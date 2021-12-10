# PoC-SOPS
POC for SOPS to encrypt different files


## Getting Started

import private key: https://github.com/LCJG-BetaLabs/PoC-SOPS/blob/master/PoC-SOPS-private.rsa

```
1. install gpg (ref: https://blog.ghostinthemachines.com/2015/03/01/how-to-use-gpg-command-line/)
2. download the file and put to <file-path>
3. gpg --import <file-path>
4. delete the file from <file-path>
```

passphrase: bet@L@bs@2O22

**(these are for demo purpose only, please do NOT put this kind of files in repository in any other case)**



### encrypt

`sops [--intput-type dotenv|json|yml] [--output-type dotenv|json|yml] -e credentials/test.env > encrypted/test.env`

### decrypt

```
# from https://github.com/mozilla/sops/issues/304#issuecomment-509238334
GPG_TTY=$(tty)
export GPG_TTY

sops [--intput-type dotenv|json|yml] [--output-type dotenv|json|yml] -d encrypted/test.env # > credentials/test.env
```

## Reference

- [Setup GPG and configure Sops](https://www.varokas.com/secrets-in-code-with-mozilla-sops/)
- [Recovery failed because no master key was able to decrypt the file](https://github.com/mozilla/sops/issues/304#issuecomment-509238334)
- [file format issue](https://github.com/mozilla/sops/issues/367)
- [export gpg private key](https://makandracards.com/makandra-orga/37763-gpg-extract-private-key-and-import-on-different-machine)

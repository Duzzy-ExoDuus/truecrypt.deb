# truecrypt-deb

> Debianization of TrueCrypt.

For installation instructions, go to: https://launchpad.net/~stefansundin/+archive/ubuntu/truecrypt

## Building

```bash
mkdir truecrypt
cd truecrypt
wget https://launchpad.net/~stefansundin/+archive/ubuntu/truecrypt/+files/truecrypt_7.1a.orig.tar.gz
tar xzf truecrypt_7.1a.orig.tar.gz
cd truecrypt-7.1a-source
git clone https://github.com/stefansundin/truecrypt-deb.git debian
debuild
```

## Bash completion for Mac OS X

The bash completion script is not perfectly compatible with Mac OS X, notably the switches with an equal sign do not behave correctly and there are errors printed.

To install with Homebrew:

```bash
ln -s /Applications/TrueCrypt.app/Contents/MacOS/TrueCrypt /usr/local/bin/truecrypt
brew install bash-completion
curl -o /usr/local/etc/bash_completion.d/truecrypt https://raw.githubusercontent.com/stefansundin/truecrypt-deb/master/truecrypt.bash-completion
```


## Stats

- [ppastats](https://stefansundin.github.io/truecrypt-deb/)
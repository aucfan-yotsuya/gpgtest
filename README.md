gpgtest
====

```
gpg --generate-key
gpg --edit-key keyid
: addkey
gpg -a -export keyid
cat > hogehoge << EOF
hogehoge
hogehoge
EOF
gpg -e -r keyid hogehoge
gpg -a -e -r keyid hogehoge
gpg --output=hogehoge -d hogehoge.gpg
gpg -s hogehoge
gpg --verify hogehoge.gpg
git add hogehoge
git commit -m "test" -Skeyid hogehoge
git push -u prod HEAD:refs/heads/branch
git log --show-signature refs/heads/branch
: master merge
git fetch -u prod -p
git log --graph prod/master
gpg --recv-key githubkeyid
gpg --edit-key githubkeyid
: tsign
git log --show-signature refs/heads/branch
: https://github.com/settings/keys
gpg -k --with-subkey-fingerprint
gpg -a --export keyid
gpg -a --export keyid | pbcopy
: regist pubkey
gpg --output=/tmp/keyring.gpg --export-secret-key
gpg --output=/tmp/subkey.gpg --export-secret-subkey keyid keyid
gpg --output=/tmp/pubkey.gpg --export
rm -rfP ~/.gnupg
gpg --import /tmp/subkey.gpg
gpg --import /tmp/pubkey.gpg
gpg --edit-key keyid
: trust
git log --show-signature refs/heads/branch
```

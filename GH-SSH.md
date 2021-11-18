```sh
cd ~

ssh-keygen -t ed25519 -C "juris@glaive.pro"
# specify a key file name, e.g. ~/.ssh/myproject-github

# If using fish:
fisher add danhper/fish-ssh-agent

ssh-add .ssh/myproject-github

cat .ssh/myproject-github.pub
```

and add the output (mby without email) to `https://github.com/<vendor>/<repo>/settings/keys/new`.

``sh
# update remote url on the repos
git remote set-url origin git@github.com:<vendor>/<repo>.git
```

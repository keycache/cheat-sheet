# Git

## Rename branch

```
git branch -m <newname>
git branch -m <oldname> <newname>
```

## Create branch from current branch

```
git checkout -b branch_name
```

## Add profile to ssh config

```
cd ~/.ssh
ssh-keygen -t rsa -C "patki.aakash@gmail.com" -f "default"
ssh-keygen -t rsa -C "patki.aakash@gmail.com" -f "apat"

pbcopy < ~/.ssh/apat.pub
pbcopy < ~/.ssh/default.pub
```

Add the files created from above command to the `ssh config`. Refer the [config file](../configs/config)

## Push a `new` repo to remote using `ssh` on a machine that has mltiple user profiles

```
git remote add origin git@github-apat:keycache/dj-drf-template.git
git push --set-upstream origin main
```

Assumption

- the local `git repository` branch is `main`
- the local ssh config file has a corresponding entry to the referenced profile. e.g.

```
Host github-apat
     HostName github.com
     User git
     IdentityFile ~/.ssh/apat
```

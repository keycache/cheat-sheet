## Git

### Push a `new` repo to remote using `ssh` on a machine that has mltiple user profiles

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

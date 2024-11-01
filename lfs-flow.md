# LFS Flows

```mermaid
flowchart TD
a[git clone source repo] --> b[from bitbucket server]
b --> c[install lfs]
c --> d[track the large files using lfs]
d --> e[add the generated artifcats ex: .gitattributes]
e --> f[commit the changes]
f --> g[run the lfs migrate]
g --> h[push to the remote origin using --force]
h --> i[expire reflogs and do cleanup]
i --> j[source repository side changes are done]
j --> k[target repository side changes - START]
k --> l[clone the target github repository]
l --> m[add the remote to bitbucket url]
m --> n[run lfs fetch an checkout to get the large file from bitbucket]
n --> o[now push the changes to the origin - github]
o --> p[end]
```

## Shell script for this
```Shell
#!/bin/sh
cd migration-test-repo
git lfs install
git lfs track "*.zip"
git add .gitattributes
git add .
git commit -m "Track large files with Git LFS"
git lfs migrate import --include="*.zip"
git push origin --force
git reflog expire --expire-unreachable=now --all
git gc --prune=now --aggressive
git push
```

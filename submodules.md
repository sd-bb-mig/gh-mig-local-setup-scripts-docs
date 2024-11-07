# Git checkout the submodules for a given repository

> If cloning a repo and need to get the submodules downloaded for the 1st time, run below command
```Shell
git submodule update --init --recursive
```

> To get the latest after cloning etc.. i.e. for the not very first time
```Shell
git submodule update --recursive
```
> or
```Shell
git pull --recurse-submodules
```

[Documentation link](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/git-submodule.html)

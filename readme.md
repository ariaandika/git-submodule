# Git Submodule

learning git submodules

Submodule is a git repo inside a git repo. Good for multiple projects.

## Add submodule

```bash
git submodule add <url>
```

## .gitmodules

it track all the submodule

it should be version controlled, pushed, and pulled.

## Submodule mangement

Pulling in Upstream Changes from the Submodule Remote

```bash
git fetch
git merge origin/main
# Here the changes also need to be commited, if the submodule remote changes
git commit -m "submodule update"
```

shortcut of fetching and merging

```bash
git submodule update --remote
```


## Cloning git repo with submodule

if we clone git with submodule, the content of the submdule will empty at first

we need to followed with another two commands:

```bash
git clone https://github.com/repo/git-with-submodule .
git submodule init
git submodule update
```

there is also a shortcut when cloning the repo

```bash
git clone --recurse-submodules https://github.com/repo/git-with-submodule .
```

## Notes

if we do git diff, the root git will not track content inside the submodule


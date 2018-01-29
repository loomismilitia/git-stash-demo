# Git Stash Demo

This is simple demonstration of the `git stash` command.

# Steps

```
cd git-stash-demo
git init
git add README.md
git commit -m "initial commit"
git checkout -b stash-branch
git add file-to-stash.txt
git commit -m "add file-to-stash.txt"
```

Edit file to add some sample text in file file-to-stash.txt

```
git add file-to-stash.txt
```

```
git checkout master
```

The following error message is displayed:

error: Your local changes to the following files would be overwritten by checkout:
	file-to-stash.txt
Please commit your changes or stash them before you switch branches.
Aborting


```
git stash
git stash list
```

Option `--index` tell the command to try to reapply the staged changes.
```
git stash apply --index
```

```
git commit -m "added sample text from stash"
```

## References

 * https://git-scm.com/book/en/v2/Git-Tools-Stashing-and-Cleaning#_git_stashing 
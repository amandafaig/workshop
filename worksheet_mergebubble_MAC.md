
Avoiding a merge bubble
======

## Easy way:

`git fetch` BEFORE pushing and pull/merge if there are upstream changes!


## Hard way:

If you accidentally commit before pulling upstream changes, and then try to pull, you'll see something like:

```
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'git@github.com:amandafaig/workshop.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

If you then pull and do a trivial merge, you'll get a commit message with something like:

```
Merge branch 'master' of github.com:user/repo
```

Annoying! Because this message provides little information. If this occurs frequently, it can clog up the history with meaningless messages

You can avoid by doing

```
git checkout -b tmp # make new temporary branch
git checkout master
git reset --hard HEAD~1
git pull
git cherry-pick tmp
git branch -D tmp
```

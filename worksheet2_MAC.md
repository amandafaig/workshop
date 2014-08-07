Exercise 3: Go back to a previous commit
====

Sometimes you want to see an old version of a file (that is, after all, the point of a version control system).  Doing this is relatively simple.

In your terminal, write `git log` to see your commit history.  If you want to go further back in time keep hitting enter.  If you see the commit you want to checkout listed, hit `q` (for "quit").

Now, choose the commit you want to go back to by typing:

```
git checkout <commit code>
```
Each commit has a unique alphanumeric code associated with it.  Typing in the first few characters (four or five) is enough for github to recognize which commit you want to go to.  While doing this exercise (in githubworkshop.git) you would type `git checkout 880f6`.

Now you've essentially gone back in time; open up your files, poke around if you want to, make changes where you want to.

When you're ready to come back to the present, type in:

```
git commit -am "message"
git checkout master
```
You will get the following message in your terminal:
```
Warning: you are leaving 1 commit behind, not connected to
any of your branches:

  <commit code> <message>

If you want to keep them by creating a new branch, this may be a good time
to do so with:

 git branch new_branch_name <command code>

Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.
```
If you want to save your new changes as a new branch (i.e. a second version of your files) you want to now type:

```
git branch <branch name> <commit code>
git push origin <branch name>
```
If you want to discard those changes, all you have to do is ignore the message and move on.

To checkout your side project (your new branch) you can do so at any time by typing

```
git checkout <branch name>
```
Your new branch is essentially a seperate (albeit similar) group of files, with the same history before you branched but different histories afterwards.  An alternate universe, perhaps?

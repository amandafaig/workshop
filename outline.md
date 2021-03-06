So far we've agreed on:

- Having a seperate workshop for each dept.
- Having the workshops in early Fall quarter (before people get bogged down).
- Having a theory aspect and a practical aspect.
- Having a set of  practical exercises
- We want to teach workflow without branching, but maybe show scenarios where branching is really useful.

## Date
right now we're tenatively planning to do these the week of Oct 6

### Practical exercises

1. Make a repo from scratch, and adding your very first file to it.

```
mkdir myrepo
cd myrepo
git init myrepo
echo "My first repo" >> README.md
git add README.md # make it so git tracks the file
git commit -m "Initial commit"
```
1. Clone (github fork) an existing repo, edit a file, and merge it properly

2. Go back to a previous commit and just play around, but exit without committing.
3. Go back to a previous commit and actually save a second copy. (figure out how to do without branching OR decide this is how we wnat to introduce branching)

4. Branching?

#### Use cases: 

Using checkout (i.e. 3 above) or just `git show <hash> path/to/file`):

A. See old version of file 
`git show <hash> path/to/file` OR if you want to do more stuff
`git checkout <hash> # now in detached head` 
B. commits (tags?) for specific figures in a ms, or (more generally) specific parameter values for generating a fig

Using checkout + saving something (or `git branch`):

A. reviving an old idea w/o branch: 

```
git show <old-hash> path/to/file > new/name
git add new/name
git commit
```

B. reviving with branch
``` 
git checkout -b new-branch-for-old-idea
git cherry-pick <old-hash> path/to/file
```


### Overall philosophy 

We seem to agree that we should stick with working from a single repo, where all members are "contributors" rather than teaching how to fork and use pull requests.

### What we need to decide/figure out/agree on:

- How much base knowledge we expect people to have.
- > AgEcon: None!  Just how to open terminal and follow instructions.
- If working on a PC is very different than working on a MAC (working with github, that is).
- > Amanda will find out next week
- How much we want to talk about in the "theory" portion

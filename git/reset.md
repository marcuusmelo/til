# Git Reset

The Git Reset command is used to undo changes. Use carefully, this is powerful.

## How to use
```git reset HEAD~X```

Where X is the number of commits you want your branch to move back.

## Example
Given the following git log:
```
4444444 - (HEAD) commit message 4
3333333 - commit message 3
2222222 - commit message 2
1111111 - commit message 1
```

if you do `git reset HEAD~2` you will endup with:

```
2222222 - (HEAD) commit message 2
1111111 - commit message 1
```

and all the changes in the commits that were removed are goig to show as unstaged changes.


## Important
This should only be done if your commits were not pushed to the shared repo yet.

If you already pushed your commit, you will need to rewrite the commit history by force pushing.
If you face yourself about to `force push` always think about 17 times and be extra careful.


## My usual use case for the git reset
I did some commits (wither just local or pushed to the origin) and I want to return my changes to a certain commit state or just to redo the commits and cleanup the git history.

## References
https://www.atlassian.com/git/tutorials/undoing-changes/git-reset

# Git Cherry Pick

The Git Cherry Pick command is used to add specific commits to your branch.

If you are in new branch based on the current state of master called branch_a and you have the commit with the hash C0mM1t in a branch b, you can use the command:

````
git cherry-pick C0mM1t

```

and the C0mM1t will now be part of branch_a. Note, you may need to solve  conflicts.

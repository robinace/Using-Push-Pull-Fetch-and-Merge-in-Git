# Using Push, Pull, Fetch, and Merge in Git
 This guide defines the `git push`, `git pull`, `git fetch`, and `git merge` commands and describes the differences between each. After reading this guide, you will be able to choose which command best fits your needs when pushing changes to or getting changes from a repository.
## Prerequisites
Before you begin, review the concepts in the following guides if needed:
- Creating and Using Repositories [xref]
- Creating and Merging Branches [xref]
## What is the difference between push, pull, fetch, and merge?
Use the following commands to:
 - `git push` send changes from your local branch to a remote repository
 - `git pull` get changes from a remote repository and merge them into your local branch
 - `git fetch` get changes from a remote repository into your tracking branch without merging them
 - `git merge` merge changes from a remote repository into your tracking branch
## Pushing to a remote repository
 `git push` makes the remote branch look like your local branch. First, the push commands checks to see whether or not there is a tracking branch. If there is an associated tracking branch, your changes are pushed from your branch to the remote branch.
### Resolving "non-fast-forward" errors
 If you do not have the most recent version of the remote repository, the "non-fast-forward updates were rejected" message appears. This message indicates that your local branch does not contain all the commits on the remote branch. When this message appears, you must sync your local branch with the remote branch using either the `git pull` or the `git fetch` and `git merge` commands described below.
## Pulling from a remote repository
 `git pull` performs a `git fetch` followed immediately by `git merge`. If you need to check changes before merging to your branch, use the `git fetch` and `git merge` commands separately, as described below.
## Fetching from a remote repository
`git fetch` takes your current branch and checks to see if there is a tracking branch. If there is an associated tracking branch, it looks for changes in the remote branch and pulls them into the tracking branch. It does not change your local branch. To merge changes to your local branch, use the `git merge` command described below.
## Merging with a remote repository
`git merge` merges the changes from the `git fetch` command described above. You would most likely need this command to merge changes made by others with changes you made to your local branch.
## Next steps
This guide describes the differences between the push, pull, fetch, and merge commands so that you can decide how to commit changes to a remote repository (`git push`) or get changes from a remote repository to your local branch (`git pull` or `git fetch` plus `git merge`).

For more information about these commands, see the following guides on GitHub:

https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository

https://docs.github.com/en/get-started/using-git/getting-changes-from-a-remote-repository

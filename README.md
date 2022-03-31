# Using Push, Pull, Fetch, and Merge in Git
 This guide defines the git push, git pull, git fetch, and git merge commands and describes the differences between each. After reading this guide, you will be able to choose which command best fits your needs when merging branches.
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
 `git push` makes the remote branch look like your local branch. First, the push commands checks to see whether or not there is a tracking branch for a remote repository connected to it. If there is an associated tracking branch, your changes are pushed from your branch to the remote branch.
### Resolving "non-fast-forward" errors
 If do not have the most recent version of the remote repository, the "non-fast-forward updates were rejected" message appears. This message indicates that your local branch does not contain all the commits on the remote branch. When this message appears, you must sync your local branch with the remote branch using either the git pull or the git fetch and git merge commands described below.
## Pulling from a remote repository
 `git pull` performs a `git fetch` followed immediately by `git merge`. If you need to check changes before merging to your branch, use the git fetch and git merge commands described below.
 
## Fetching from a remote repository
`git fetch` again takes our current branch, and checks to see if there is a tracking branch. If so, it looks for changes in the remote branch, and pulls them into the tracking branch. It does not change your local branch.

## Merging with a remote repository
 To do that, you'll need to do `git merge origin/master` (for the "master" branch) to merge those changes into your branch - probably also called "master".

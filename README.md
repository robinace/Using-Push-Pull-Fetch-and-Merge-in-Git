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
 `git push` takes our current branch, and checks to see whether or not there is a tracking branch for a remote repository connected to it. If so, your changes are taken from your branch and pushed to the remote branch. This is how code is shared with a remote repository, you can think of it as "make the remote branch resemble my local branch". This will fail if the remote branch has diverged from your local branch: if not all the commits in the remote branch are in your local branch. When this happens, your local branch needs to be synchronized with the remote branch with git pull or git fetch and git merge.

## Pulling from a remote repository
 Often `git push` and `git pull` are described as equivalent. This isn't entirely correct, since under the hood `git pull` does two things. `git pull` simply does a `git fetch` followed immediately by `git merge`. This is often what you desire to do, but you may prefer to use git fetch followed by git merge to make sure you understand the changes you are merging into their branch before the merge happens.

## Fetching from a remote repository
`git fetch` again takes our current branch, and checks to see if there is a tracking branch. If so, it looks for changes in the remote branch, and pulls them into the tracking branch. It does not change your local branch.

## Merging with a remote repository
 To do that, you'll need to do `git merge origin/master` (for the "master" branch) to merge those changes into your branch - probably also called "master".

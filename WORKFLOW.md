**Git Team Sync Workflow**



**1. What did the rejected push error say, and why did it happen?**



\-The rejected push error said that my local branch was behind its remote counterpart and that the remote contained work that was not present locally. Git rejected the push 		because the push would not be a fast-forward update.



\-This happened because another clone pushed changes to the same shared branch before my local clone pushed its changes. My local branch was therefore outdated.



**2. What is the difference between the merge in Task 3 and the rebase in Task 4?**



\-In Task 3, I used `git merge` to combine the changes from the remote feature branch with my local changes. This resulted in a merge commit that preserved both lines of 	history.



\-In Task 4, I used `git rebase` after fetching the updated remote branch. Rebase replayed my local commit on top of the updated remote history, producing a more linear history 	instead of creating another merge commit.



**3. What is one habit that would have avoided both rejected pushes?**



\-One useful habit is to fetch or pull the latest changes from the remote branch before starting work and before pushing. Keeping the local branch synchronized helps prevent 	working from an outdated branch.



**4. Which approach would you default to on a shared team branch, and why?**



\-I would generally use merge on a shared team branch because it preserves the existing shared history and does not rewrite commits that other developers may already have based 	their work on. Rebase can be useful for keeping a personal branch history linear, but it should be used carefully on branches that are already shared.




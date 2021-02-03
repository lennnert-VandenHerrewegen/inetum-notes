# Git

## Commits
`git commit -v` - Show changes in commit
`git commit -a` - Commit all unstaged changes
`git commit -m ""` - Commit directly with a message

## Log
`git log -2` - Two most recent commits
`git log -p` - Show patch for each commit
`git log --pretty=oneline` - prettify
`git log --pretty=full` - prettify
`git log --pretty=fuller` - prettify
`git log --since "2 months"`
`git log --until "2 months"`
`git log --graph`

## Revert
`git commit --amend` - Amend staged changes to last commit
`git revert f3286bd03ee16b863129d0aaca8c0387d645d0b7` - Revert commit (You don't have to enter the entire hash)

## Cloning
`git clone <repo-url>`

## Remote repo's
`git remote`
`git remote add new-remote http://new-remote-example.com`
`git fetch origin`
`git merge origin master`
`git pull` - combine fetch and merge
`git push origin master`
`git remote show origin` - More info about configured remote

## Tags
`git tag` - List all tags
`git tag --list <glob>` - Show all tags matching glob
`git tag "1.0"` - Tag commit
`git tag -a "1.1" -m "This is my new annotated tag"` - Create (a)nnotated flag
`git push origin 1.1` - Push specific tag
`git push origin --tags` - Push all tags

## Branches
`git branch <branch-name>` - Create new branch on current commit
`git checkout <branch-name>` - Go to new branch
`git checkout -b <branch-name>`- Create and checkout new branch
`git merge <branch>` - Merge a branch into HEAD
`git push <remote> <branch-name>`
`git checkout <remote> <branch>` - 
`git checkout -b branchname remote/branchname` - Create remote tracking branch
`git checkout --track origin/branch-name` - Create remote tracking branch
`git push --delete branch` - Delete a remote branch

### Rebasing
Combining two branches that doesn't create a merge commit
Replays the commits from a feature branch on top of the target branch
`git rebase master`
never rebase public branches onto feature

## Forking
1. `git remote add upstream git@github.com:test/test.git`
2. `git remote -v show`
3. `git fetch upstream`
4. `git merge upstream/master` - Merge upstream into fork

## Squashing commits
Merging several commits together
1. `git reset --soft HEAD~5` - Undo last 5 commits and keep them as unstaged changes
2. `git status`
3. `git diff --staged`
4. `git commit -v`
Be careful about squashing commits once you have pushed

## Merge requests
`git push origin modify-readme`


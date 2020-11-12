## Keeping Pull Requests clean:
- Note that this is a semi-advanced topic. Make sure you are somewhat familiar with using git and/or try this on repositories you control before actually using it publically.
### Creating a fork to make edits on:
On github, click fork
- `git clone FORKURL`
- `git checkout -b patch-NAME`
### Making changes:
make changes, `git add FILE`, `git commit`, `git status`, etc to add new commits
### Pull new changes made from original repo to your fork
- `git remote add upstream FORKED` where FORKED is the git clone url for the original repo that was forked
- `git fetch upstream`
- `git rebase upstream/master` or whatever the name of the upstream branch you want to update to is
- use `git log` to verify
- `git push origin`

Actually pulling new changes:
- `git pull upstream master` then `git commit` to update from the forked git
	- These commits will disappear when you use rebase at the end
### Making the actual pull request
- make pull request within github's GUI
  - On your repo there may be a notification asking if you want to create a pull request
  - You can also go to the original repo, pull requests and create on there

__**DO NOT EVER EVER EVER REBASE ON NON-PULL-REQUEST REPOS/BRANCHES**__

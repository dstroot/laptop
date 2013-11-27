# My Changes

## How to track updates from the original repository.  

First you have to add the original repository as a source. Let's use "upstream" to designate the original repository.

`git remote add upstream https://github.com/thoughtbot/laptop.git`

This adds the remote repository. You can use `git remote -v` to see your remotes. There should be “origin” already, pointing to your GitHub fork. The new remote repository should be listed as "upstream".

Now when you whan to pull in changes from the original repository you can do it a couple ways. 

### First way: 

`git fetch upstream`

This loads all commits, including branches and tags, from the specified remote repository, using the alias defined above.

`git merge upstream/master master`

This merges all changes from the original master branch in your current branch, eg. your local master branch.

### Second way:

All in one command.  Note "git pull" which is fetch + merge

`$ git pull upstream master`

### Third way:

Better yet, replay your local work on top of the fetched branch

`$ git rebase upstream/master`
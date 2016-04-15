# Git
Switching remote URLs from SSH to HTTPS

Open Terminal.

Change the current working directory to your local project.

List your existing remotes in order to get the name of the remote you want to change.

git remote -v
origin  git@github.com:USERNAME/REPOSITORY.git (fetch)
origin  git@github.com:USERNAME/REPOSITORY.git (push)
Change your remote's URL from SSH to HTTPS with the git remote set-url command.

git remote set-url origin https://github.com/USERNAME/OTHERREPOSITORY.git
Verify that the remote URL has changed.

git remote -v
# Verify new remote URL
origin  https://github.com/USERNAME/OTHERREPOSITORY.git (fetch)
origin  https://github.com/USERNAME/OTHERREPOSITORY.git (push)
The next time you git fetch, git pull, or git push to the remote repository, you'll be asked for your GitHub username and password.

If you have two-factor authentication enabled, you must create a personal access token to use instead of your GitHub password.
You can use a credential helper so Git will remember your GitHub username and password every time it talks to GitHub.

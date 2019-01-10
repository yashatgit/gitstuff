# Collection of handy git commands

### Remote repositories
A remote URL is Git's fancy way of saying "the place where your code is stored." That URL could be your repository on GitHub, or another user's fork, or even on a completely different server.

Use `git remote -v` to list all the listed remotes for that particular repository.

### Creating a new remote [...](https://help.github.com/articles/about-remote-repositories/)
```
git remote add origin  <REMOTE_URL> 
```
This associates the name `origin` with the `REMOTE_URL` which can be a [HTTPS or SSH address](https://help.github.com/articles/which-remote-url-should-i-use/).

### Adding a new remote [...](https://help.github.com/articles/adding-a-remote/)
To add a new remote, use the `git remote add` command on the terminal, in the directory your repository is stored at. This command takes two arguments:
* A remote name, for example, `origin`
* A remote URL, for example, `https://github.com/user/repo.git`

For example
```
$ git remote add origin https://github.com/user/repo.git
# Set a new remote
$ git remote -v
# Verify new remote
origin  https://github.com/user/repo.git (fetch)
origin  https://github.com/user/repo.git (push)
```


### Changing a remote's URL [...](https://help.github.com/articles/changing-a-remote-s-url/)
The `git remote set-url <existing_remote_name> <new_remote_url>` command changes an existing remote repository URL.
```
$ git remote -v
origin  git@github.com:USERNAME/REPOSITORY.git (fetch)
origin  git@github.com:USERNAME/REPOSITORY.git (push)

$ git remote set-url origin https://github.com/USERNAME/REPOSITORY.git

$ git remote -v
# Verify new remote URL
origin  https://github.com/USERNAME/REPOSITORY.git (fetch)
origin  https://github.com/USERNAME/REPOSITORY.git (push)
```

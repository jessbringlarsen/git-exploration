# git-exploration
For documenting learnings and experiments with git

## Configuring git
The configuration [manual](htps://git-scm.com/book/tr/v2/Customizing-Git-Git-Configuration)

    man git-config

### The three levels of configurations
 - system, configuration is system wide and valid for all users on a system
 - global, for a specific user and all of the users repositories
 - local, for a single repository

Configuration command examples:

    git config --global --list
    git config --global --edit
    git config --global core.editor vim
    git config --global user.name jebla
    git config --global user.email jebla@jebla.dk
    
### Configuration of credential cache
[git-credential-cache](https://git-scm.com/docs/git-credential-cache) - Helper to temporarily store passwords in memory

    git help credentials

    git config credential-helper cache 
    .. commit and push, and at some point exit the daemon
    git config credential-helper exit

### SSL configuration
If your git server is using a self signed certificate then you might experience issues with pushing to the repo. To disable ssl certificate verfication _for a specific_ repository not global or system wide, issue this command:

    git config --local http.sslVerify false

## Working with branches
To checkout a remote branch fetch the existing branches and view the available branches:

    git fetch
    git branch -v -a
    
After that just checkout the branch out the branch to work on:
    git checkout <branch>

# git-exploration
For documenting learnings and experiments with git

## Configuring git
The configuration [manual](htps://git-scm.com/book/tr/v2/Customizing-Git-Git-Configuration)

    man git-config

### The three levels of configurations
 - system, configuration is system wide and valid for all users on a system
 - global, for a specific user and all of the users repositories
 - local, for a single repository

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

# Git Config
As you read briefly in Getting Started, you can specify Git configuration settings with the git config command. One of the first things you did was set up your name and email address:
```Bash
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com

# list git config
git config --list
```

Now you’ll learn a few of the more interesting options that you can set in this manner to customize your Git usage.

First, a quick review: Git uses a series of configuration files to determine non-default behavior that you may want. The first place Git looks for these values is in the system-wide [path]/etc/gitconfig file, which contains settings that are applied to every user on the system and all of their repositories. If you pass the option --system to git config, it reads and writes from this file specifically.

The next place Git looks is the ~/.gitconfig (or ~/.config/git/config) file, which is specific to each user. You can make Git read and write to this file by passing the --global option.

Finally, Git looks for configuration values in the configuration file in the Git directory (.git/config) of whatever repository you’re currently using. These values are specific to that single repository, and represent passing the --local option to git config. If you don’t specify which level you want to work with, this is the default.

Each of these “levels” (system, global, local) overwrites values in the previous level, so values in .git/config trump those in [path]/etc/gitconfig, for instance.

# Reference
[Git](https://git-scm.com/)  
[Git Config Guide]()
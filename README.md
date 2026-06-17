1. what is git --> git is a distributed version control system, it's a tool that helps developers to track changes in files.

## we have 3 types of version control systems

1. local version control system. --> History stored only on our machine - (your laptop/computer) if we laptop has damaged you will loss the data.
2. centralised version control system --> A single central system has stored our history, if that central system is down, whatever devices are conneted with that those are not work.
3. distributed version control system --> every developer has a complete copy of the repository including the history.

### git commands list

1.  # **git status** - It checks where you are

    problems: 1. which branch you are in. 2. which files changed. 3. which files are staged, 4. untracked files.
    it will compare **working directory vs staging area vs last commit**

2.  ## **git branch - current branch **

        This command will helps to know, to show all branches in your local and it shows which branch you are in with (*) mark - current branch.

3.  **#. git diff - see what changed**
    you changed code but forgot excatly what -- it will compares working directory with last staged version.

**4. stage chages --> git add . (all files), git add file_name (only particular file).**

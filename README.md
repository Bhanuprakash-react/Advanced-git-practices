1. what is git --> git is a distributed version control system, it's a tool that helps developers to track changes in files.

## we have 3 types of version control systems

1. local version control system. --> History stored only on our machine - (your laptop/computer) if we laptop has damaged you will loss the data.

2. centralised version control system --> A single central system has stored our history, if that central system is down, whatever devices are conneted with that those are not work.

3. distributed version control system --> every developer has a complete copy of the repository including the history.

### git commands list

1.  Repository commands:
    1. git init --> Creates a new git repository in the current folder.

    2. git clone url --> download an existing repository in our local with history.

    3. git config --global user.name "Bhanuprakash-react" --> To set username globally.

    4. git config --global user.email "bhanuprakash4015@gmail.com" --> to set email globally.

2.  Status and Inspection commands:
    1. git status --> It shows current branch, modified branch, staged files and, untracked files.
       it will compares [working directory vs staging area vs last commit]
       unstaged files represted as in red colour, staged files shown in colour as green.

    2. git diff --> see what changed, you changed code but forgot what you changed.
       It will compare working directory vs staging area.

    3. git diff --staged --> shows staged changes before commiting.

    4. git log --> This command will show the complete information of the commit history.
       It display all commits with commit id, commit messgae, author name, author mail id, date & time.

    5. git log --oneline --> It Displays all the commit history in a compact manner.

    6. git show commitId --> commit id means, every commit it will creates a unique commit id,
       if we run this command it will the complete details of that particular commit.

    7. git show --> It shows details about last commit (It shows the head commit).

3.  Staging commands:
    1. git add filename.js --> staging a specific file for commit.

    2. git add . --> This command staged all files in the working directory.

    3. git restore --staged filename.js --> Remove a file from staging without losing changes.

    4. git restore filename.js --> Remove a file from staged and as well as in working directory also.

4.  Commit Commands:
    1. git commit -m "message" --> It creates a commit from staged changes.

    2. git commit --amend or git commit --amend -m "message" --> modify the most recent commit and modify the commit message also.

    3. git commit --am "message" --> Stage tracked files and commits in one command. - shortcut for (git add . and git commit -m "message").

5.  Branch Commands:
    1. git branch --> List local branches.

    2. git branch -a --> List local and remote branches.

    3. git branch -r --> List remote branches only.

    4. git branch --show-current --> show current branch.

    5. git branch feature-x --> It creates a new branch.

    6. git branch -m old new --> this command will helps is to rename the existig the branch name.

    7. git branch -d feature-x --> Deletes a merged branch

    8. git branch -D feature-x --> Forcefully deletes the branch.

6.  Switch/Checkout Commands:
    1. git switch main --> this command will helps us to switch or move existing branch in local.

    2. git switch -c git-practices --> this command will help us to create and switches to new branch.

    3. git checkout main --> older command to switch branches.

    4. git checkout -b git-practices --> older command to create and switch to new branch.

7.  Merge commands:
    1. git merge feature-x --> Merge feature-x into our current branch

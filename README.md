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
    1. git merge feature-x --> Merge feature-x into our current branch (branch-1 and branch-2 --> we need branch-1 code in branch-2 -->
       lets switch into branch-2 and run the command git merge branch-1 --> it will merge branch-1 in branch-2).

    2. git merge --abort --> It cancels merge in progress. (branch-1 and branch-2 both are working in same file...and did changes in same line
       --> if we try to merge branch-1 in branch-2 --> it shows a merge conflicts --> then 1. if its possible to resolve that , you can
       --> otherwise , if its seems like too clumsy just abort it so that branch-2 changes will wipe out from branch-1).

8.  Remote commands:
    1. git remote -v --> it will shows the connected remote repositories.

    2. git remote add origin url --> it connects local repo to remote repository.

    3. git remote remove origin --> removes a remote connection.(intially take pull from another repo --> run git remote -v to shows the connected repos or current repo --> you need to cut it run git remote remove origin (it does not delete the repo and code only disconnected with that repo --> for new connection run git remote add origin url --> then push our code safely to new repo.) )

    4. git remote set-url origin url --> (if suppose you changed the repo name in github git-practices to advanced-git-practice --> before that existing url connected to local is git-practices not advanvced-git-practices (for check git remote -v) --> for this suitation just add git remote set-url origin url(adv-git-practices) --> it will connected the changed repo --> otherwise push and pull will not happen with existing repo.)

9.  Push Commands:
    1. git push --> It uploads local commits to the remote repository. (once -u origin main rans it knows the handshake so simple it moves from local branch -renote branch and it shows pull requests in github).

    2. git push origin main -->push main branch to github. (It tells where you have to go every single time)

    3. git push -u origin main -->pushes and sets upstream tracking branch.(create branch 1st time we use it)

    4. git push --force --> Forcefully overwrites remote branch history.

    5. git push --force-with-lease --> safer version of force push.

    1st create a branch --> work and commit it --> use git push -u origin main (1st time) --> and then work - commit in same branch --> use git push.

10. Pull and Fetch Commands:
    1. git fetch --> Downloads remote changes without merging.

    2. git pull --> Downloads and merges remote changes.

    3. git pull origin main --> pull latest changes from main branch.

    main(remote) -- dev(safety branch) --> developer-1 --> git clone url (dev) --> create another branch -->home-page(feature-branch)--
    --> develop the feature --> switch to dev branch --> take git pull from dev for latest updates --> sitch to feature branch and then merge dev into feature branch --> then push origin home-page (it will shows pull request in github).

    git fetch:

    git fetch --> 2 developers working on same branch --> developer -2 completed his work and push it to dev-->developer-1 is not completed in the middle --> but developer needs to check what he did --> use git fetch --> to check the changes he did.

11. UNDO commands:
    1. git restore filename.js --> if we written some code in code editor, and if we dont want that before running any commands,
       like git add . or git commit --> we run git restore filename.js --> it will remove code from in our code editor.

    2. git restore --staged filename.js --> if suppose we run the command git add . --> but we have to revert it from stagged to unstagged --> so then we should use git restore --staged filename.js.

    3. git restore . --> Discard all uncommitted changes.

    4. git reset --soft HEAD~1 --> this command will help if we commit too quickly, to forget few lines of code--> so we need to add or change commit message.

    5. git reset HEAD~1 or git reset mixed HEAD~1 --> git reser --soft HEAD~1 this command will undo the commit but its in stagged --> if our
       code uncommit and unstagged at a time we should use the command git reset HEAD~1 or git reset mixed HEAD~1

    6.
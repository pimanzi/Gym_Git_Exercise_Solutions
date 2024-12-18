# GYM_GIT_EXERCISE_SOLUTIONS

## BUNDLE 1

### EXERCISE 1

```Bash
$ mkdir Gym_Git_Exercise_Solutions/
$ cd Gym_Git_Exercise_Solutions/
/Gym_Git_Exercise_Solutions$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint: 	git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint: 	git branch -m <name>
Initialized empty Git repository in /home/pimanzi/Documents/Gym_Git_Exercise_Solutions/.git/
/Gym_Git_Exercise_Solutions$ touch hello.js
/Gym_Git_Exercise_Solutions$ rm hello.js
/Gym_Git_Exercise_Solutions$ vi school.js
/Gym_Git_Exercise_Solutions$ ls
school.js
/Gym_Git_Exercise_Solutions$ git add .
/Gym_Git_Exercise_Solutions$ git commit -m "adding and deleting files"
[master (root-commit) 943c525] adding and deleting files
 1 file changed, 1 insertion(+)
 create mode 100644 school.js
/Gym_Git_Exercise_Solutions$ git branch
* master
/Gym_Git_Exercise_Solutions$ git branch -m master main
/Gym_Git_Exercise_Solutions$ git branch
* main
/Gym_Git_Exercise_Solutions$ git status
On branch main
nothing to commit, working tree clean
/Gym_Git_Exercise_Solutions$ git add .
/Gym_Git_Exercise_Solutions$ git commit -m "renamed my branch"
On branch main
nothing to commit, working tree clean
/Gym_Git_Exercise_Solutions$ git remote add origin https://github.com/pimanzi/Gym_Git_Exercise_Solutions.git
/Gym_Git_Exercise_Solutions$ git push -u origin main
Username for 'https://github.com': pimanzi
Password for 'https://pimanzi@github.com':
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 224 bytes | 224.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/pimanzi/Gym_Git_Exercise_Solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
/Gym_Git_Exercise_Solutions$ git checkout -b dev
Switched to a new branch 'dev'
/Gym_Git_Exercise_Solutions$ git branch test
/Gym_Git_Exercise_Solutions$ git branch
* dev
  main
  test
/Gym_Git_Exercise_Solutions$ git branch -d test
Deleted branch test (was 943c525).
/Gym_Git_Exercise_Solutions$ git branch
* dev
  main
/Gym_Git_Exercise_Solutions$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

/Gym_Git_Exercise_Solutions$ git push -u origin dev
Username for 'https://github.com': pimanzi
Password for 'https://pimanzi@github.com':
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/pimanzi/Gym_Git_Exercise_Solutions/pull/new/dev
remote:
To https://github.com/pimanzi/Gym_Git_Exercise_Solutions.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'
```

## BUNDLE 1

### EXERCISE 2

```Bash
~/Gym_Git_Exercise_Solutions$ touch home.html
~/Gym_Git_Exercise_Solutions$ git add home.html
~/Gym_Git_Exercise_Solutions$ git stash save "Added home.html"
Saved working directory and index state On main: Added home.html
~/Gym_Git_Exercise_Solutions$ touch about.html
~/Gym_Git_Exercise_Solutions$ git add .
~/Gym_Git_Exercise_Solutions$ git stash save "Added about.html"
Saved working directory and index state On main: Added about.html
~/Gym_Git_Exercise_Solutions$ git git stash list
git: 'git' is not a git command. See 'git --help'.

The most similar command is
        init
~/Gym_Git_Exercise_Solutions$ git stash list
stash@{0}: On main: Added about.html
stash@{1}: On main: Added home.html
~/Gym_Git_Exercise_Solutions$ touch touch team.html
~/Gym_Git_Exercise_Solutions$  touch team.html
~/Gym_Git_Exercise_Solutions$ git stash list
stash@{0}: On main: Added about.html
stash@{1}: On main: Added home.html
~/Gym_Git_Exercise_Solutions$ git stash save "Added team.html"
No local changes to save
~/Gym_Git_Exercise_Solutions$ git add .
~/Gym_Git_Exercise_Solutions$ git stash save "Added team.html"
Saved working directory and index state On main: Added team.html
~/Gym_Git_Exercise_Solutions$ git stash list
stash@{0}: On main: Added team.html
stash@{1}: On main: Added about.html
stash@{2}: On main: Added home.html
~/Gym_Git_Exercise_Solutions$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (dc2176fd88f91e967129c81f6c9733df7e0d126b)
~/Gym_Git_Exercise_Solutions$ git stash list
stash@{0}: On main: Added team.html
stash@{1}: On main: Added home.html
~/Gym_Git_Exercise_Solutions$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (6011b6061b4d4722927c7784fba39e90c9f874a9)
~/Gym_Git_Exercise_Solutions$ git add .
~/Gym_Git_Exercise_Solutions$ git commit -m "adding html files"
[main 377d7d9] adding html files
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
~/Gym_Git_Exercise_Solutions$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 537 bytes | 537.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/pimanzi/Gym_Git_Exercise_Solutions.git
   207fbdb..377d7d9  main -> main
~/Gym_Git_Exercise_Solutions$ git stash list
stash@{0}: On main: Added team.html
~/Gym_Git_Exercise_Solutions$ git stash pop stash@{0}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (8cfd0d560cc04ba963441af61deb59ade5ebaf76)
~/Gym_Git_Exercise_Solutions$ git reset --hard HEAD
HEAD is now at 377d7d9 adding html files
~/Gym_Git_Exercise_Solutions$
```

## BUNDLE 2

### EXERCISE 1

```Bash

/Gym_Git_Exercise_Solutions$ git branch
* main
/Gym_Git_Exercise_Solutions$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
/Gym_Git_Exercise_Solutions$
/Gym_Git_Exercise_Solutions$ touch services.html
/Gym_Git_Exercise_Solutions$ git add .
/Gym_Git_Exercise_Solutions$ git commit -m "added service page"
[ft/bundle-2 56f91cd] added service page
 1 file changed, 11 insertions(+)
 create mode 100644 services.html
/Gym_Git_Exercise_Solutions$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

/Gym_Git_Exercise_Solutions$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 444 bytes | 444.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/pimanzi/Gym_Git_Exercise_Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/pimanzi/Gym_Git_Exercise_Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
/Gym_Git_Exercise_Solutions$
```

## BUNDLE 2

### EXERCISE 2

````Bash

## BUNDLE 2

### EXERCISE 1

```Bash

/Gym_Git_Exercise_Solutions$ git branch
* main
/Gym_Git_Exercise_Solutions$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
/Gym_Git_Exercise_Solutions$
/Gym_Git_Exercise_Solutions$ touch services.html
/Gym_Git_Exercise_Solutions$ git add .
/Gym_Git_Exercise_Solutions$ git commit -m "added service page"
[ft/bundle-2 56f91cd] added service page
 1 file changed, 11 insertions(+)
 create mode 100644 services.html
/Gym_Git_Exercise_Solutions$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

/Gym_Git_Exercise_Solutions$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 444 bytes | 444.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/pimanzi/Gym_Git_Exercise_Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/pimanzi/Gym_Git_Exercise_Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
/Gym_Git_Exercise_Solutions$
````

```

```

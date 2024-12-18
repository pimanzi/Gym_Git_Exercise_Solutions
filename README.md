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

### EXERCISE 2

```Bash

/git checkout -b main
 1978  git checkout main
 1980  git add .
 1981  git commit -m "updaing readme"
 1982  git push
 1984  git checkout main
 1985  git pull
 1986  git checkout -b ft/service-redesign
 1987  git add .
 1988  git commit -m "added services list"
 1989  git push
 1990  git push --set-upstream origin ft/service-redesign
 1991  git checkout main
 1992  git add .
 1993  git commit -m "adding new services list"
 1994  git push
 1995  git checkout ft/service-redesign
 1996  git merge main
 1997  git add .
 1998  git commit
 1999  git push
```

## BUNDLE 3

### EXERCISE 1

```Bash

git branch
 2016  git checkout main
 2017  git checkout -b ft/team-page
 2020  git add .
 2021  git commit -m "adding a team page"
 2022  git push
 2023  git push --set-upstream origin ft/team-page
 2024  git checkout main
 2025  git checkout -b ft/contact-page
 2026  git checkout ft/team-page
 2027  git log
 2028  git checkout ft/contact-page
 2029  git cherry-pick 00942489dc09fc0407344d2114f4bea1365d3bf3
 2030  git add .
 2031  git commit -m "adding pages"
 2032  git push
 2033  git branch
 2034  git checkout -b ft/faq-page
 2035  git add .
 2036  git pcommt -m "adding faq page"
 2037  git pcommit -m "adding faq page"
 2038  git commit -m "adding faq page"
 2039  git push
 2040  git push --set-upstream origin ft/faq-page
 2041  git revert 00942489dc09fc0407344d2114f4bea1365d3bf3
 2042  git add .
 2043  git commit -m "removing the team page"
 2044  git push
```

### EXERCISE 2

```Bash

 git branch
 2062  git checkout ft/faq-page
 2064  git branch
 2066  git checkout -b ft/home-page-redesign
 2067  git checkout main
 2068  git add .
 2069  git commit -m "changing the about html"
 2070  git push
 2071  git checkout ft/home-page-redesign
 2072  git rebase main
```

## Bundle 4

### EXERCISE 1

```Bash
 git branch
 2082  git remote add git-copy https://github.com/pimanzi/Gym_Git_Exercises_Clone.git
 2084  git add .
 2085  git commit -m "updating home page"
 2086  git push
 2088  git push
 2089  git push git-copy
```

### EXERCISE 2

```Bash
2104  git checkout -b ft/footer
 2106  git add .
 2107  git commit -m "added footer page"
 2108  git add .
 2109  git commit -m "changed the footer"
 2110  git push
 2111  git checkout main
 2112  git checkout -b ft/squashing
 2113  git merge --squash ft/footer
 2114  git status
 2115  git commit -m "adding a footer page"
 2116  git push
```

## Bundle 5

### Exercise 1

Successfully enabled github pages on my repo passing in settings

### Exercise 2

git add .
git commit -m "changed the index html header"
git push

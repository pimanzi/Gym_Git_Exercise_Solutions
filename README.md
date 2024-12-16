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

# Steps

techcombd remote name : upstream
your remote name: origin

1. Fork the repository

2. Clone the forked repository to your computer

```
git clone [your_forked_repository_url/ssh_link]
```

Example:

```
git clone git@github.com:ratanparai/first-contributions.git
```

3. Now `cd` into the cloned folder-

```
cd first-contributions
```

3. add upstream remote-

```
git remote add upstream [upstream_url]
```

Example: for our first-contributions repository-

```
git remote add upstream https://github.com/techcombd/first-contributions.git
```

Check if the upstream remote added succesfully-

```
git remote -v
```

You should see something like this-

```
origin  git@github.com:ratanparai/first-contributions.git (fetch)
origin  git@github.com:ratanparai/first-contributions.git (push)
upstream        https://github.com/techcombd/first-contributions.git (fetch)
upstream        https://github.com/techcombd/first-contributions.git (push)
```

4. fetch upstream branch-

```
git fetch upstream
```

**Note:** This command fetch the upstream branch into your local disk. You can see those by running-

```
git branch -a
```

3. set upstream for master branch

```
git branch -u upstream/master
```

Now when you run-

```
git status
```

you should see something like-

```
On branch master
Your branch is behind 'upstream/master' by 14 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

nothing to commit, working tree clean
```

Now push change to your forked repository(origin)-

```
git push origin master
```

To know more read [Git Branching - Remote Branches](https://git-scm.com/book/en/v2/Git-Branching-Remote-Branches)

4. create new branch. follow standard. not mendatory

```
git checkout -b feature/add-ratanparai
```

6. link the branch with origin remote's branch

```
git push -u origin feature/add-ratanparai
```

7. made changes to files (do what you want to do for the work)
8. `add` and `commit` changes

```
git add .
git commit -m "write your commit message here"
```

9. push changes

```
git push
```

10. rebase upstream changes to your current brunch
- `git checkout master`
- `git pull`
- `git checkout feature/add-name`
- `git rebase master`
11. `git fetch upstream`
12. `git rebase upstream/master`
13. fix merge conflict if there is any.
14. push changes to origin brunch
10. go to your forked location `github.com/yourname/first-contribution`.
11. click `create pull request`
12. refresh the page and sign CLA (contributor's license aggrement)
13. wait for maintainer's reply
14. if the maintainer need any change then do so in your working branch
15. add, commit, and push changes
16. wait for maintainer's response
17. if maintainer says everything okay. and merge the changes then delete your brunch
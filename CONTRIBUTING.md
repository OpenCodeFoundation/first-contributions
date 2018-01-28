# How to contribute

Before going deep into the steps please remember you **DO NOT NEED** to follow the remote name we used. You can use anything you want. You need to change your command depending on the name you choose.

- **upstream** - Remote name of `techcomdbd`'s repository.
- **origin** - Remote name of your forked repository.

## Steps for doing a pull request

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

Pull changes from upstream (if there is any) -

```
git pull
```

Now push change to your forked repository(origin)-

```
git push origin master
```

To know more read [Git Branching - Remote Branches](https://git-scm.com/book/en/v2/Git-Branching-Remote-Branches)

4. create new branch. follow standard **(Not Mandatory)**

```
git checkout -b feature/add-ratanparai
```

6. Push the branch to your origin(forked) repository while linking the branch with origin's remote branch

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

10. Go to your url page you should see something like-

![pull-request](images/compareandpull.png)

Click **Compare & pull request** to start the `pull request` process. In the next page give your pull request a easy to understand title and clear description what you are trying add to the project.

## WORK IN PROGRESS
> **NOTE:** Bellow this line is work in progress documentation.


10. rebase upstream changes to your current brunch
- `git checkout master`
- `git pull`
- `git checkout feature/[your-branch-name]`
- `git rebase master`

11. If there is any conflict resolve it.

10. go to your forked location `github.com/yourname/first-contribution`.
11. click `create pull request`
12. refresh the page and sign CLA (contributor's license aggrement)
13. wait for maintainer's reply
14. if the maintainer need any change then do so in your working branch
15. add, commit, and push changes
16. wait for maintainer's response
17. if maintainer says everything okay. and merge the changes then delete your brunch
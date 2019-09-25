# Git Exercises

## First Set
1. Create a new directory on your Desktop called git_exercises and cd into that directory.
2. Using `git init`, create a new repository.
3. Using the `touch` command, create empty files called foo and bar in your repository directory.
4. Enter `ls` to make sure they were added.
5. Check your `git status`.
6. Using `git add foo`, add `foo` to the staging area. Confirm with `git status` that it worked.
7. Using `git commit -m` add an appropriate message, add foo to the repository.
8. Check your `git status`.
9. Using `git add bar`, add bar to staging area. Confirm with git status that it worked.
10. Now run `git commit -m` option, and add the message `“Add bar”`.
11. Using `git log`, confirm that the commits made in the previous exercises worked correctly.

## Solution First Set
  Last login: Tue Sep 24 22:04:16 on ttys000
Cassidys-MacBook-Air:~ cassidy_beni$ cd Desktop
Cassidys-MacBook-Air:Desktop cassidy_beni$ git clone https://github.com/cassidybeni/git-lab.git
Cloning into 'git-lab'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 1 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
Cassidys-MacBook-Air:Desktop cassidy_beni$ mkdir git_exercises
Cassidys-MacBook-Air:Desktop cassidy_beni$ cd git_exercises
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git init
Initialized empty Git repository in /Users/cassidy_beni/Desktop/git_exercises/.git/
Cassidys-MacBook-Air:git_exercises cassidy_beni$ touch foo.md bar.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ ls
bar.md	foo.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	bar.md
	foo.md

nothing added to commit but untracked files present (use "git add" to track)
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git add foo.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   foo.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	bar.md

Cassidys-MacBook-Air:git_exercises cassidy_beni$ git commit -m "foo staging"
[master (root-commit) b4fdc82] foo staging
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 foo.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	bar.md

nothing added to commit but untracked files present (use "git add" to track)
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git add bar
fatal: pathspec 'bar' did not match any files
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git add bar.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git commit -m "Add bar"
[master 63ca48f] Add bar
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 bar.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git log
commit 63ca48f091892d7dd3a4b14e9e2a4d88d5856bc5 (HEAD -> master)
Author: Cassidy Beni <cassidybeni@pursuit.org>
Date:   Tue Sep 24 22:19:41 2019 -0400

    Add bar

commit b4fdc828025ead99e8306a8a5321a13cba131b05
Author: Cassidy Beni <cassidybeni@pursuit.org>
Date:   Tue Sep 24 22:18:38 2019 -0400

    foo staging
Cassidys-MacBook-Air:git_exercises cassidy_beni$ 


## Second Set

1. Use touch to create an empty file called baz.
2. Check that it's there by entering `ls`.
3. Check the status of your git. 
4. Add baz to the staging area using `git add .`, then commit with the message `"Add bazz"`.
5. Realizing there’s a typo in your commit message, change bazz to baz using `git commit --amend -m Add baz`.
6. Run git log to get the id of the last commit, then view the diff using `git show <id>` to verify that the message was amended properly.

## Solution Second Set 

Cassidys-MacBook-Air:git_exercises cassidy_beni$ touch baz.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ ls
bar.md	baz.md	foo.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	baz.md

nothing added to commit but untracked files present (use "git add" to track)
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git add .
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   baz.md

Cassidys-MacBook-Air:git_exercises cassidy_beni$ git commit "add bazz"
error: pathspec 'add bazz' did not match any file(s) known to git
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git commit -m "bazz"
[master 6bfdf9b] bazz
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 baz.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git commit --amend -m Add baz
error: pathspec 'baz' did not match any file(s) known to git
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git commit --amend -m "Add baz"
[master d0be98d] Add baz
 Date: Tue Sep 24 22:25:44 2019 -0400
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 baz.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git log
commit d0be98ddc3df99ae94b20650f14bc9b2ccd849c8 (HEAD -> master)
Author: Cassidy Beni <cassidybeni@pursuit.org>
Date:   Tue Sep 24 22:25:44 2019 -0400

    Add baz

commit 63ca48f091892d7dd3a4b14e9e2a4d88d5856bc5
Author: Cassidy Beni <cassidybeni@pursuit.org>
Date:   Tue Sep 24 22:19:41 2019 -0400

    Add bar

commit b4fdc828025ead99e8306a8a5321a13cba131b05
Author: Cassidy Beni <cassidybeni@pursuit.org>
Date:   Tue Sep 24 22:18:38 2019 -0400

    foo staging
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git show b4fdc828025ead99e8306a8a5321a13cba131b05
commit b4fdc828025ead99e8306a8a5321a13cba131b05
Author: Cassidy Beni <cassidybeni@pursuit.org>
Date:   Tue Sep 24 22:18:38 2019 -0400

    foo staging

diff --git a/foo.md b/foo.md
new file mode 100644
index 0000000..e69de29
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git show d0be98ddc3df99ae94b20650f14bc9b2ccd849c8
commit d0be98ddc3df99ae94b20650f14bc9b2ccd849c8 (HEAD -> master)
Author: Cassidy Beni <cassidybeni@pursuit.org>
Date:   Tue Sep 24 22:25:44 2019 -0400

    Add baz

diff --git a/baz.md b/baz.md
new file mode 100644
index 0000000..e69de29
Cassidys-MacBook-Air:git_exercises cassidy_beni$ 



### Third Set

1. The `git log` command shows only the commit messages, which makes for a compact display but isn’t particularly detailed. Verify by running `git log -p` that the `-p` option shows the full diffs represented by each commit. Press `q` to escape.
2. Create a file `README.md`, add and commit it.
3. Got to github and create a new repository. Connect your local repo to the remote one.
4. Open your README.md and and add the line `# hello there` at the top of `README.md` and save.
5. Check the status, then add, check the status, and then commit the new line with a commit message of your choice. Verify using `git status` that the change was committed as expected.
6. Push your changes: `git push origin master`. Refresh your github and click on the commit to verify the changes.

## Third Solution Set 
Last login: Wed Sep 25 18:09:16 on ttys000
Cassidys-MacBook-Air:~ cassidy_beni$ cd Desktop
Cassidys-MacBook-Air:Desktop cassidy_beni$ cd git_exercises
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git log -p
commit d0be98ddc3df99ae94b20650f14bc9b2ccd849c8 (HEAD -> master)
Author: Cassidy Beni <cassidybeni@pursuit.org>
Date:   Tue Sep 24 22:25:44 2019 -0400

    Add baz

diff --git a/baz.md b/baz.md
new file mode 100644
index 0000000..e69de29

commit 63ca48f091892d7dd3a4b14e9e2a4d88d5856bc5
Author: Cassidy Beni <cassidybeni@pursuit.org>
Date:   Tue Sep 24 22:19:41 2019 -0400

    Add bar

diff --git a/bar.md b/bar.md
new file mode 100644
index 0000000..e69de29

commit b4fdc828025ead99e8306a8a5321a13cba131b05
Author: Cassidy Beni <cassidybeni@pursuit.org>
Date:   Tue Sep 24 22:18:38 2019 -0400
Cassidys-MacBook-Air:git_exercises cassidy_beni$ touch README.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md

nothing added to commit but untracked files present (use "git add" to track)
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git add README.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   README.md

Cassidys-MacBook-Air:git_exercises cassidy_beni$ git commit -m "commit README"
[master a2317c4] commit README
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git remote add origin https://github.com/cassidybeni/Git-Exercise.git
Cassidys-MacBook-Air:git_exercises cassidy_beni$ code README.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git add README.md
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   README.md

Cassidys-MacBook-Air:git_exercises cassidy_beni$ git commit -m "git exercise"
[master a50e8df] git exercise
 1 file changed, 1 insertion(+)
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git status
On branch master
nothing to commit, working tree clean
Cassidys-MacBook-Air:git_exercises cassidy_beni$ git push origin master
Enumerating objects: 12, done.
Counting objects: 100% (12/12), done.
Delta compression using up to 4 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (12/12), 1.02 KiB | 1.02 MiB/s, done.
Total 12 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), done.
To https://github.com/cassidybeni/Git-Exercise.git
 * [new branch]      master -> master



### Fourth Set

1. Using the markdown below, add a line at the end of the README with a link to the official Git documentation:

```markdown
~/repos/website/README.md
 For more information on Git, see the
[official Git documentation](https://git-scm.com/).
```

2. Commit your change with an appropriate message. Why not?

3. Push your change to GitHub. By refreshing your browser, confirm that the new line has been added to the rendered README. Click on the “official Git documentation” link to verify that it works.

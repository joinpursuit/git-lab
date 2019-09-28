# Git Exercises

## First Set
1. Create a new directory on your Desktop called git_exercises and cd into that directory.
cd Desktop
mkdir git_exercises
cd git_exercises/
2. Using `git init`, create a new repository.
git init
3. Using the `touch` command, create empty files called foo and bar in your repository directory.
touch foo.js
touch bar.js
4. Enter `ls` to make sure they were added.
ls
5. Check your `git status`.
git status
6. Using `git add foo`, add `foo` to the staging area. Confirm with `git status` that it worked.
git add foo.js
git status
7. Using `git commit -m` add an appropriate message, add foo to the repository.
git commit -m "that foo"
8. Check your `git status`.
git status
9. Using `git add bar`, add bar to staging area. Confirm with git status that it worked.
git add bar
git status
10. Now run `git commit -m` option, and add the message `“Add bar”`.
git commit -m "Add bar"
11. Using `git log`, confirm that the commits made in the previous exercises worked correctly.
git log
commit e99e805e0b56f69b56448e159b7eca8a629e4f5c (HEAD -> master)
Author: syn perez <synperez@putsuit.org>
Date:   Fri Sep 27 23:01:30 2019 -0400

    Add bar

commit ec04fced9b3340976822819351aefc96273c0576
Author: syn perez <synperez@putsuit.org>
Date:   Fri Sep 27 22:59:15 2019 -0400

    that foo

  

## Second Set

1. Use touch to create an empty file called baz.
touch baz.js
2. Check that it's there by entering `ls`.
ls
3. Check the status of your git. 
git status
4. Add baz to the staging area using `git add .`, then commit with the message `"Add bazz"`.
git add baz.js
git commit -m "Add bazz"
5. Realizing there’s a typo in your commit message, change bazz to baz using `git commit --amend -m Add baz`.
git commit baz.js --amend -m "add baz"
6. Run git log to get the id of the last commit, then view the diff using `git show <id>` to verify that the message was amended properly.
git log
git show
commit 565fc29f205cccb5dbe4d73bbc163f2a8365326c (HEAD -> master)
Author: syn perez <synperez@putsuit.org>
Date:   Fri Sep 27 23:05:59 2019 -0400

    add baz

diff --git a/baz.js b/baz.js
new file mode 100644
index 0000000..e69de29

### Third Set

1. The `git log` command shows only the commit messages, which makes for a compact display but isn’t particularly detailed. Verify by running `git log -p` that the `-p` option shows the full diffs represented by each commit. Press `q` to escape.
git log -p
//q
2. Create a file `README.md`, add and commit it.
touch README.md
git add README.md
git commit -m "read me"
3. Got to github and create a new repository. Connect your local repo to the remote one.
git remote add origin https://github.com/synperez/Git-lab-set-third-set.git
git push -u origin master
4. Open your README.md and and add the line `# hello there` at the top of `README.md` and save.
//added # hello there to README.md
5. Check the status, then add, check the status, and then commit the new line with a commit message of your choice. Verify using `git status` that the change was committed as expected.
git status
git add README.md
git status
git commit -m "obi wan"
git status

6. Push your changes: `git push origin master`. Refresh your github and click on the commit to verify the changes.
git push origin master`

### Fourth Set

1. Using the markdown below, add a line at the end of the README with a link to the official Git documentation:

```markdown
~/repos/website/README.md
 For more information on Git, see the
[official Git documentation](https://git-scm.com/).
```

code .
//added copied text
git status
git add README.md
git status
git commit -m "fourth set firmware update"
git status
git push
//made a mistake, fixed it
code .
//updated copied text
git status
git add README.md
git status
git commit -m "fourth set firmware update ver 2"
git status
git push

2. Commit your change with an appropriate message. Why not?

3. Push your change to GitHub. By refreshing your browser, confirm that the new line has been added to the rendered README. Click on the “official Git documentation” link to verify that it works.

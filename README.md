# Git Exercises

## First Set
1. Create a new directory on your Desktop called git_exercises and cd into that directory.
```
mkdir git_exercises
cd git_exercises
```
2. Using `git init`, create a new repository.
```
git init
```
3. Using the `touch` command, create empty files called foo and bar in your repository directory.
```
touch foo
touch bar
```
4. Enter `ls` to make sure they were added.
```
ls
```
5. Check your `git status`.
```
git status
```
6. Using `git add foo`, add `foo` to the staging area. Confirm with `git status` that it worked.
``` 
git add foo
git status
```
7. Using `git commit -m` add an appropriate message, add foo to the repository.
```
git commit -m "add foo"
```
8. Check your `git status`.
```
git status
```
9. Using `git add bar`, add bar to staging area. Confirm with git status that it worked.
```
git add bar
git status
```
10. Now run `git commit -m` option, and add the message `“Add bar”`
```
git commit -m "add bar"
```
11. Using `git log`, confirm that the commits made in the previous exercises worked correctly.
```
git log
```

  

## Second Set

1. Use touch to create an empty file called baz.
```
touch baz
```
2. Check that it's there by entering `ls`.
```
ls
```
3. Check the status of your git. 
```
git status
```
4. Add baz to the staging area using `git add .`, then commit with the message `"Add bazz"`.
```
git add .
git commit -m "Add bazz"
```
5. Realizing there’s a typo in your commit message, change bazz to baz using `git commit --amend -m Add baz`.
```
git commit --amend -m add baz
```
6. Run git log to get the id of the last commit, then view the diff using `git show <id>` to verify that the message was amended properly.
```
git show 27540765abd2b2d2664367c003cfa1678dcc697b
```

### Third Set

1. The `git log` command shows only the commit messages, which makes for a compact display but isn’t particularly detailed. Verify by running `git log -p` that the `-p` option shows the full diffs represented by each commit. Press `q` to escape.
``` 
git log -p
q
```
2. Create a file `README.md`, add and commit it.
```
touch README.md
git add README.md
git commit -m "create README"
```
3. Got to github and create a new repository. Connect your local repo to the remote one.
4. Open your README.md and and add the line `# hello there` at the top of `README.md` and save.
5. Check the status, then add, check the status, and then commit the new line with a commit message of your choice. Verify using `git status` that the change was committed as expected.
6. Push your changes: `git push origin master`. Refresh your github and click on the commit to verify the changes.

### Fourth Set

1. Using the markdown below, add a line at the end of the README with a link to the official Git documentation:

```markdown
~/repos/website/README.md
 For more information on Git, see the
[official Git documentation](https://git-scm.com/).
```

2. Commit your change with an appropriate message. Why not?

3. Push your change to GitHub. By refreshing your browser, confirm that the new line has been added to the rendered README. Click on the “official Git documentation” link to verify that it works.

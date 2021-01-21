## General

- install : https://git-scm.com/download/
- setting ~/.gitconfig
- Git needs the following information to know who commits

```bash
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

- When you `git init`, a branch called `master` is create

## Starting point

- create a repository
  `git init`
- track files
  `git add *.c`
- clone a repository
  `git clone rep yourfolder(optional)`

each file has two states: tracked or untracked

once tracked it has two states: modified and unmodifed

Once commited, it's called staged

If modified but not commited, you see the following notification when running `git status`. Note the red text.

![](img/pro_git/2021-01-21-20-06-42.png)

Run `git add file` to stage the file (which doesn't mean it's commited)

If you modify a file after you run git add, you have to run git add again to stage the latest version of the file. See the following snapshot:

![](img/pro_git/2021-01-21-20-10-21.png)

The `contributing.md` is both staged and not staged because it has been modified since the last `git add`

Use `git status -s` to get a concise report.

💯 Setting up a `.gitignore` file for your new repository **before** you get going is generally a good idea. `/` is to avoir recursivity and `/` at the end is to specify a directory. An exemple:

![](img/pro_git/2021-01-21-20-16-05.png)

For python template, see [here](https://github.com/github/gitignore/blob/master/Python.gitignore). For other languages, see [here](https://github.com/github/gitignore)

## Intermediate

`git diff` by itself doesn’t show all changes made since your last commit — only changes that are still unstaged. If you’ve staged all of your changes, `git diff` will give you no output.
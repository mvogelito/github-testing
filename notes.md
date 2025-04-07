
Create project directory and content

At command line in the root af that directory, initialize this local directory:
`git init -b main`

Note this creates folder `.git` that is hidden in VSCode. Subdirs `hooks`, `info`, `objects`, `refs`.  Files `config`, `description`, and `HEAD`.

Add all files to new local repository: stages them for the first commit:

`git add .`

And do the commit:

`git commit -m "First commit"`

Output:
```
[main (root-commit) 13cccff] First commit
 3 files changed, 8 insertions(+)
 create mode 100644 index.html
 create mode 100644 notes.md
 create mode 100644 readme.md
 ```

Then logged on to GitHub from CLI:  

`gh auth login`

and basically followed prompts.  This set up GitHub via git:

```
✓ Authentication complete.
- gh config set -h github.com git_protocol https
✓ Configured git protocol
✓ Logged in as mvogelito
```

Used GitHub CLI to create the repository on GH:

`gh repo create --source=. --private`

```
✓ Created repository mvogelito/github-testing on GitHub
✓ Added remote https://github.com/mvogelito/github-testing.git
```

Since I used `gh` to create repo, I didn't have to do:

`git remote add origin https://github.com/mvogelito/github-testing.git`

And could test that it was already set up with:

`git remote -v`

And then push to github:

`git push origin main`

With output:

```
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (7/7), 538 bytes | 538.00 KiB/s, done.
Total 7 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/mvogelito/github-testing.git
 * [new branch]      main -> main
 ```





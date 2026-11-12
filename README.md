# Practice-of-version-control "to view in pointwise the open in edit mode"
This is practice of all git commands
git init initializes a new Git repository in the current folder to start tracking changes.
cat README.md displays the contents of the README.md file in the terminal.
cat > README.md creates or overwrites the file
cat >> README.md adds new content to the end of the file.
git remote -v displays the URLs of all remote repositories connected to your local Git repository (fetch and push).and shows which GitHub repository your local project is connected to.
origin  https://github.com/username/project.git (fetch)
origin  https://github.com/username/project.git (push)  
origin = nickname of your GitHub repository.
fetch = URL used to download changes from GitHub.
push = URL used to upload changes to GitHub.
git fetch → Downloads the latest changes from GitHub but does not apply them to your working files.
git pull → Downloads changes from GitHub AND applies them to your local project.
shows your local Git repository is successfully connected to your GitHub repository.
git remote add origin URL(of github) connects your local Git repository to a GitHub repository.
The folder from which you run Git Bash is your local project folder.
If you have executed git init inside that folder, it becomes a local Git repository.
.git folder: Stores Git's tracking information and history.
git status shows the current condition of your local Git repository, including which files are modified, newly created, staged, or not yet committed.
in its output:On branch main → You are currently working on the main branch.
No commits yet → You have not saved any changes in Git history yet.
Untracked files → Git has detected two files but is not tracking them yet:
Nothing added to commit → You haven't added any files to the staging area.
git add . Adds both files to the staging area.  then git commit -m "first commit" then git push origin main
The staging area is a place where you temporarily keep the selected files that you want to include in your next commit.
you want to commit index.html and style.css. then :git add index.html style.css git commit -m "Added homepage"
git commit -m "[Vanya]add: readme file added" saves the staged changes permanently in your local Git repository with a descriptive message.
git commit -m "[Vanya]add: readme file added"  its output is below:
main (root-commit) 0072fe8] [Vanya]add: readme file added
 2 files changed, 4 insertions(+)
 create mode 100644 readme.md
 create mode 100644 this is readme  meaning of the above output is:
 1. main → You committed changes on the main branch.
2. root-commit → This is the first commit in your repository.
3. 0072fe8 → Unique short ID of your commit.
4. [Vanya]add: readme file added → Your commit message.
5. 2 files changed → Two files were included in the commit.
6. 4 insertions(+) → Four lines of content were added.
7. create mode 100644 → Git created and started tracking these files.
Important: Your changes are saved locally, but they are not yet uploaded to GitHub.

working tree clean → No uncommitted changes exist in your project folder.
To upload them, run:git push -u origin main
git branch -m practice renames your current branch from main to practice.
git checkout -b practice creates a new branch named practice and immediately switches you to it
git switch -c practice creates a new branch named practice and immediately switches to it.

to dlete a file in branch from local folder as well a from github:git rm filename
git commit -m "delete: file removed"
git push origin practice

***** delete branch****  git branch -a   git push origin --delete practice
touch index.html This creates the file in your local project folder.   ,,, to add the content echo "<h1>Hello World</h1>" > index.html ,,, ls to check file,, git add index.html,git commit -m "add: index.html file", git push origin main

to rename file  git mv oldfilename newfilename   git commit -m "rename: index.html to home.html"  git push origin main
```
To make a folder along with file inside it :mkdir HTML  touch HTML/index.html
git add HTML/  git commit -m "add: HTML folder created"    git push origin main
rm -r HTML to delete folder locaally
git rm -r --cached HTML
git commit -m "delete folder from GitHub"
git push origin main  to delete only from github not locally

git rm -r HTML git commit -m "delete: HTML folder removed"  git push origin main   to delete from both the places


```
 


# Git-cheatsheet
---

# Git commands for new repository 

## Setup
```
git config --global user.name "your_name"
```
```
git config --global user.email "your_email"
```
// to edit name and email
```
git config --global --edit
```

// For creating new folder:-
```
mkdir New_folder
```
```
cd New_folder/
```


By using git add it comes from working directory to staging area and after commit it is send to the repository <br>
// initialize new git repository <br>
// add all the files in the current directory at once using "." or can mention <Filenames> to be added <br>
// git commit to commit the repository using a message from the said action <br>
// select the branch name to be included in the default display on first commit <br>
// add the url of the repository <br>
// push the changes to be displayed on the github platform <br> 
```
git init
```

```
git add .
```

```
git commit -m "first commit"
```

```
git branch -M main
```

```
git remote add origin <url.git>
```

```
git push -u origin main
```
<br><br><br>
// show active changes & status
```
git status
```
// view commit history
```
git log
```
// list local branches
```
git branch
```
// create a new branch
```
git branch <branch-name>
```
// switch to new branch
```
git checkout <branch-name>
```
// switch & create a new branch
```
git checkout  -b <branch-name>
```
// merge changes from a branch
```
git merge <branch-name>
```
// delete a branch
```
git branch -D <branch-name>
```
// pull change code on github
```
git pull
```
// fetch changes without merging
```
git fetch
```
// discard active changes
```
git reset --hard HEAD
```
// revert changes in a commit
```
git revert <commit-hash>
```

To push into github:-
```
git remote -v
git remote add origin 
git remote -v
git branch -M master
git push -u origin master
```
<br><br><br>
In Git, rebasing is a process that integrates changes from one branch into another. It’s an alternative to the merge command and is used to create a clean, linear history of commits. When you rebase a branch, you’re moving all the changes that have been committed on one branch and replaying them on the tip of another branch
Here’s a simplified explanation of how rebasing works:

- Git finds the common base commit between the two branches.
- It then takes the diff introduced by each commit of the branch being rebased.
- These changes are saved to temporary files.
- The branch you are rebasing is reset to the same commit as the branch you are rebasing onto.
- Finally, Git applies each change in turn.
- This results in a history that appears linear, as if all the work happened in series, even if it originally happened in parallel. It’s particularly useful when you want to maintain a clean project history or when preparing to contribute to a project by ensuring your commits apply cleanly on a remote branch12.

Here’s a basic command sequence for rebasing:
```
$ git checkout feature-branch
$ git rebase master
```
This sequence checks out the feature-branch and rebases it onto the master branch, making it as if the changes in feature-branch were made starting from the latest commit in master

For error 403:-
```
git config --global --unset-all credential.helper
```
```
git config --unset-all credential.helper
```

# How to create a git repository and add to GitHub

## Summary of steps
1. Initialise new repo locally and in GitHub ('git init').
2. Stage files to be comitted ('git add [file]').
3. Commit staged files ('git commit -m '[commit message]'').
4. Add origin ('git remote add origin [link to GitHub repo]').
5. Push to GitHub ('git push -u origin main').

## Initialise new repository locally and in GitHub
1. Log into GitHub and use the '+' symbol (top right) to create a new empty repo. 
2. Create a new local directory for the project (use 'mkdir [name]' in the command line). Open VS Code in that new directory (use 'code .' in the command line).
3. Open a new terminal in VS Code and run 'git init'. This is initialise an empty git repo. Run 'ls -a' to get a list of all files, including the hidden .git file to confirm this.

## Adding files
1. Create a new file in the directory. Usually start with README.md. Add some content. 
2. Run 'git status' to see the new file as 'untracked'. 
3. Stage files for commit: run 'git add *' to stage all files, or 'git add [file name] to stage individual files. Run 'git status' again to confirm which files have been staged.
3. Commit staged files: run 'git commit -m '[commit message]''. 
4. Change the default branch in GitHub to 'main' - run 'git branch -M main'.
5. Connect the local repo to GitHub: run 'git remote add origin [link to GitHub repo]' and if necessary follow links to log in to GitHub through VS Code.  
6. Push to commit to GitHub: run 'git push -u origin main' (-u is shorthand for set upstream which tells VS Code which remote repo to push it to. This only needs to be done once. Any subsequent pushes will push to that upstream.

### Further commits to the same branch
7. Only need to repeat staging, commit and push. 

## Branching
1. Create a new branch: run 'git checkout -b [name of branch]'. NB 'git checkout [branch] switches branch. If you include -b it will create a new branch. Run 'git branch' to view branches and check which one you are on. (Add -v or -vv for more information).
2. Make changes to files, save and stage (run 'git add [file]').
3. Commit changes (run 'git commit -m '[message]').
4. Push commit to GitHub. Will need to set upstream for the new feature branch. Run 'git push -u origin feature branch'. Refresh GitHub to see new branch and click 'compare and pull request'. Follow the GitHub workflow to accept and merge changes. Delete feature branch in GitHub.
5. Merge and update locally: 
    Run 'git fetch origin'.
    Run 'git checkout main'.
    Run 'git merge origin/main'.
    Or 'git pull' is shorthand for 'git fetch' and 'git merge'.
6. Delete feature branch locally. Run 'git branch -d [branch]'.

### To do locally rather than following pull-request work-flow
7. Create a new branch, stage and commit changes as above. 
8. Switch to main branch - 'git checkout main'.
9. Then merge - 'git merge [branch]'.
10. Then push the merged main branch to GitHub. 

# Tags

1. Tags are a pointer to a particular commit. Use to label milestones / versions. Tags are immutable so you can use them to revisit previous versions etc. 
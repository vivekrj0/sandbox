
### Development workflow

Branches are one of the basic concepts of git. There is a main branch `master`, and new branches are created out of the main master branch. Every branch represents a feature you are working on, and it has different series of commits. Once a feature is complete, the new branch is `merged` into the master branch.

Branches allow us to work on more than 1 feature at the same time, thus helping us avoid mixing of commits. If during the process, there are useless commits added and the whole branch is messed up, you can easily delete the branch and create a fresh branch from the main `master` branch.

Note: **Never ever commit or rebase on your master branch**.

The development workflow goes like this :

1. Clone the repo.
2. Cd into the repo.
3. Currently, you are on your master branch. Suppose you want to work on a feature X, (e.g.,Adding background image on the home page), you should a create a new branch with some name of your choice, with:    

    `git branch <branch-name>`    
    And then, checkout to the branch you created by:
    
    `git checkout <branch-name>`
    This brings you to your new branch \<branch-name>.
    
4. Now, open up your text editor, make some changes to the files you want to, save it. When you have made a considerable amount of change, `commit`. You should commit neither too often nor too late.

    The process of commiting goes like this:
    
    `git status` : This shows the status of your files, i.e. it shows which files are present in the staging area and which are not.
    
    `git add <path/to/file>` : This adds the selected files to the staging area. To add, all the files to staging area, do `git add .`
    
    `git commit` : On doing this, a text editor opens up and you are asked to enter a commmit message. Commit message should be short (less than 50 characters), and should convey what change you have made. Keep the commit message as meaningful as possible.
    
5. You have successfully committed your changes. You can add a few more commits, and then push these changes to your remote repository by :
    `git push origin <branch-name>`.    
    Note that all these changes took place in your created branch \<branch-name> , and you can delete whatever changes you made by deleting the branch. The above command pushed youur code online to your github repository.
    
6. Go to github's online repository and you can see an option of `Compare and Pull request` against your recently pushed branches. Make a Pull request by entering a short meaningful message and a meaningful comment about what your pull request does.

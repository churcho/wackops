# How we collaborate using branching at The Funding Floor 
At The Funding Floor when working on code we use modified version of the Git Workflow that is simply 

Create a private branch off a public branch.
Regularly commit your work to this private branch.
Once your code is working, clean up its history.
Merge the cleaned-up branch back into the public branch.


## Default Branches
1. build - private
2. develop  - public/private
3. master - public  


## How to Use the Branches 
- When working on a feature a developer needs to create private feature branch off of master as mentioned above try to keep commits to this branch regular and small. Try and name the branches in an informatie matter e.g `feature/user_authentication` rather than `auth`. other prefixes to consider are `bug/ patch/ docs/` the point is to be as informative to the reviewer as possible

- If your work takes multiple days be sure to clean up the branches history by rebasing it on the latest `public` branch for in our case this would be `master` 

- Whenever you need to demo some work publicly feel free to merge into `build`, for this reason build is considered a `private` branch since it may contain some unreviewed work 

- Once you are done with your work please open a pull request to the `develop` branch so that it can be peer reviewed and eventually get merged. 

- Once work has been merged into `develop` it may undergo further review and maybe even go backwards in the pipeline although usually the case is it gets approved and is scheduled for a `release cycle`

## Peer Reviews 
So what do you do when requested to review some changes…

First and foremost is to pull the git branch on which the changes have been made, with the list of all the files that have the changes to be reviewed. Start your review, GitHub provides in-line comments thus a reviewer can comment on a specific lines of code in a given file. It also provides a back and forth forum where the collaborators can discuss the changes made to the file.

Depending on the changes made, the reviewer can request further changes or approve the changes made. This goes on and on until the desired code is achieved; one benefit of this kind of banter is that anyone working on the project can see the changes made.

Tools such as git blame allow the viewing of the previous versions of the same file and git-rebase which allows undoing unwanted commits.

## Release Cycles 
At the moment we are doing releases to both `develop` which is our `staging` enviroment every week and the same period for releases to `master`






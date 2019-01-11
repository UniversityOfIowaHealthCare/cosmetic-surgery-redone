# University of Iowa Health Care - Cosmetic Surgery

## Cloning
1) Run the usual `git clone git@github.com:UniversityOfIowaHealthCare/cosmetic-surgery-redone.git` command
2) Then, because the theme is actually a git submodule (hugo is weird) you need to:
    1) From the root directory of the project run `cd themes`
    2) Run `git submodule init`
    3) `git submodule update`
3) Everything should be up to date, so run `hugo serve` and view the page!   

## Contributing
This section serves as an outline for how to add code to this repo. It's a fairly simple process: create a feature branch for your feature, make commits (and keep that branch up to date with origin/dev by [rebasing](https://git-scm.com/docs/git-rebase)), PR it into the dev branch, then celebrate once your PR is approved and merged into dev. The master branch is reserved for releases - it mirrors what is currently in production. 

### Overview
* **We never commit directly to either master or dev**
    * Master mirrors prod while dev houses newly accepted code (to be merged into master on release)
* We use rebasing to keep feature branches up to date
* We squash commits when we merge PRs
* Approval from at least one reviewer is required before a PR can be merged
* **Always feel free to ask any questions you have or to challenge this process if you have ideas to improve it**


### In-depth & step-by-step:
1) Identify the feature/fix you're adding to the site
2) Make sure your local `dev` branch is update to date with the remote version of `dev`
3) From that local `dev` branch, create a feature branch: `git checkout -b name-of-my-feature-or-fix`
4) Do your code magic
5) Make commits of your code magic 
6) Frequently make sure your feature branch is up to date with `origin/dev`, and **always do this via rebase**: `git pull --rebase origin dev`
7) Push your branch to GitHub: `git push origin name-of-my-feature-or-fix`
8) Create a pull request to merge your branch into `dev`
    * > Hint: we squash all commits from a feature branch into 1 single commit when it's merged into `dev` in order to keep things more clear. The name of your PR will be used as that single commit's message, so name it accordingly.
9) Your PR will be reviewed. Revise as needed, then celebrate once it's approved and merged
10) When it's time, someone with the power will merge your code from `dev` into `master` and your code will be in production!

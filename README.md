# University of Iowa Healthcare - Cosmetic Surgery

## Cloning
1) Run the usual `git clone git@github.com:UniversityOfIowaHealthCare/cosmetic-surgery-redone.git` command
2) Then, because the theme is actually a git submodule (hugo is weird) you need to:
    1) From the root directory of the project run `cd themes`
    2) Run `git submodule init`
    3) `git submodule update`
3) Everything should be up to date, so run `hugo serve` and view the page!    

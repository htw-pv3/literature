# Steps done until now in GitBash and GitHub

## Git Setup Configuration in GitBash (Open GitBash as Admin)

### Your Identity
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com

### Your Editor Programm
git config --global core.editor "'C:/Programme_RE/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"

### Checking Your Settings
git config --list

### Checking and Edit The Global Settings
git config --global --edit

### Open in your Editor the file bash.bashrc from the Directory C:\Git\etc\ and Add at the end of the file the following lines:
# start from
cd C:/git/github;

## Check that you are under C:/git/github/htw-pv3) otherwise write
cd C:/git/github/htw-pv3

## Cloning the Repository literature in htw-pv3/literature:
git clone https://github.com/htw-pv3/literature.git

## Cloning the Repository wheather-data in htw-pv3/weather-data:
 git clone https://github.com/htw-pv3/weather-data.git

## going inside the directory literature (C:/git/github/htw-pv3/literature), it will change to master
cd literature

## Checking the Status of the Files and the changes
git status

## Checking the Status and the changes associated with users and Structure of branches (Tree form with content and code)
gitk

## Update of the Info in the Folder (Download all the updated files from the server)
git pull

## Changing the name or extention of a File
git mv git_cheat_sheet.txt git_cheat_sheet.md

## TRACKING New Files or STAGING Modified Files: with git add is a multipurpose command — you use it to begin tracking new files, to stage files, and to do other things 
## like marking merge-conflicted files as resolved. It may be helpful to think of it more as “add precisely this content 
## to the next commit” rather than “add this file to the project”
git add git_cheat_sheet.md

## Confirm or committing the changes with a message -m and jumping the git add with -a (Adding the -a option to the git commit
## command makes Git automatically stage every file that is already tracked before doing the commit, letting you skip the 
## git add part from before). It is important to leave a space before # to give the Hashtag or Ticketnumber
git commit -a -m "Changing the File extention #6" 

## Uploading all local commits (changes) to the GitHub server
git push

## Creating a new File in the actual Folder and open it with the editor
start notepad++ Codes_GitBash_So_Far.md

## Removing a File 
git rm Codes_GitBash_So_Far.md

## Commiting the delete of the file
git commit -m "remove the File #6"

## See all the Branches
git branch -av

## Creatung a new Branch
git checkout -b feature/gitbash-code-so-far#10

## Creating a new File in the actual Branch
start notepad++ Codes_GitBash_So_Far.md

## Staging the created and Modified File (Tracking the File)
git add Codes_GitBash_So_Far.md

## Commiting (Contribute) The Tracked changes
git commit -m "GitBash_Code_So_Far #10"
## Or jumping the step of tracking the File just with -a
git commit -a -m "GitBash_Code_So_Far #10"

## Upload the remote changes (Commits) for a review and follow with a PullRequest(PR)
git push --set-upstream origin feature/gitbash-code-so-far#10

## Deleting a Remote Branch if you push the branch already and have mistakes
git push origin --delete feature/gitbash-code-so-far#10

## Deleting a Local Branch with mistakes
git checkout master 
git branch -D feature/gitbash-code-so-far-#10

## Staging and commiting the Modified File (Updates) before merge (Tracking the File)
git commit -a -m "GitBash_Code_So_Far #10"

## Merge the branch after Positiv Review of members
git merge feature/gitbash-code-so-far#10

## Deleting a Remote Branch if you push the branch already
git push origin --delete feature/gitbash-code-so-far#10

## Deleting a Local Branch 
git checkout master 
git branch -D feature/gitbash-code-so-far#10
 
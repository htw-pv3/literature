# Crib Sheet - GIT

# Cheat Sheet Collection

## git

[git-cheat-sheet by github](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)

[git-cheat-sheet by tower](https://user-images.githubusercontent.com/14353512/80648952-5fb73080-8a71-11ea-8c5a-1297b1c4a9fd.png)

## Git Setup Configuration in GitBash (Open GitBash as Admin)

### Your Identity
git config --global user.name "John Doe" <br>
git config --global user.email johndoe@example.com

### Your Editor Programm
git config --global core.editor "'C:/Programme_RE/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"

### Checking Your Settings
git config --list

### Checking and Edit The Global Settings
git config --global --edit

### Open in your Editor the file bash.bashrc from the Directory C:\Git\etc\ and Add at the end of the file the following lines:
start from
cd C:/git/github;

## Check that you are under C:/git/github/htw-pv3, otherwise write
cd C:/git/github/htw-pv3

## Cloning the Repository literature in htw-pv3/literature:
git clone https://github.com/htw-pv3/literature.git

		Guide: how to clone
		1. Create the desired folder structure on your computer with the directory you want to clone into
		2. Start git-bash and navigate with the "cd" command" into the created directory
		3. Go to github.com to the appropriate repository (in this case https://github.com/htw-pv3/literature) and click on the green drop down button called "code" in the top left corner and copy the https
		4. enter the command "git clone" in git-bash with the link (git clone https://github.com/htw-pv3/literature.git)
		
## Cloning the Repository wheather-data in htw-pv3/weather-data:
 git clone https://github.com/htw-pv3/weather-data.git

## Going inside the directory literature (C:/git/github/htw-pv3/literature), it will change to master
cd literature

## Checking the Status of the Files and the changes
git status

## Checking the Status and the changes associated with users and Structure of branches (Tree form with content and code)
gitk

## Update of the Info in the Folder (Download all the updated files from the server)
git pull

## Changing the name or extention of a File
git mv git_cheat_sheet.txt git_cheat_sheet.md

## TRACKING New Files or STAGING Modified Files: with git add is a multipurpose command — you use it to begin tracking new files, to stage files, and to do other things like marking merge-conflicted files as resolved. It may be helpful to think of it more as “add precisely this content to the next commit” rather than “add this file to the project”
git add git_cheat_sheet.md

## Confirm or committing the changes with a message -m and jumping the git add with -a (Adding the -a option to the git commit command makes Git automatically stage every file that is already tracked before doing the commit, letting you skip the git add part from before). It is important to leave a space before # to give the Hashtag or Ticketnumber
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
git branch -a

## Creating a new Branch
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

## Deleting a Remote Branch (Just if you had a mistake and you push (Published) the branch already)
git push origin --delete feature/gitbash-code-so-far#10
## Or
git branch -dr feature/gitbash-code-so-far-#10

## Deleting a Local Branch with mistakes (Just if you had a mistake)
git checkout master
git branch -D feature/gitbash-code-so-far-#10

## Staging and commiting the Modified File (Updates) before merge (Tracking the File)
git commit -a -m "GitBash_Code_So_Far #10"

## Upload the remote changes (Commits) to the remote already created PullRequest(PR)
git push --set-upstream origin feature/gitbash-code-so-far-#10

## Merge the branch after Positiv Review of members (has to be done in GitHub GUI or try the following):
git merge --no--ff feature/gitbash-code-so-far-#10

## Closing an issue related to the PR in the same repository
close #issue_number

## Changing to the master Branch
git checkout master

## Update the changes in the Repository (Folder) (Download all the updated files from the remote server)
git pull


# denotes a comment and should not be entered with it

# Show all branches
git branch -a

# Show all upstreams
git remote show origin

# Switch to branch
git checkout #branch_name

# Switch to branch and create if it does not exist
git checkout -b #branch_name

# Check changes on the server (server->local)
git fetch

# Transfer change from server (server->local->merge)
git pull

# Transfer changes to the server (local->server)
git push

# Transfer changes to a new branch on the server (local->server)
git push -u origin #branch_name

# Add file to the tracking
git add #file

# Display changes of a specific file
git log --follow #file

# Commit all tracked changes
git commit -m „#your_comment“

# Admin
git config --global core.editor „‘D:/Notepad++/notepad++.exe‘ -multiInst -notabbar -nosession -noPlugin“

# Information Display Command Guide
git help

# Literature on Git 

Git is an open source version control system. 
The following links contain tutorials for git and github. 
They summarize essential features of the software and show the most common commands, especially for git bash.

1. Title: **Hello World - Github Guides**

   - URL: https://guides.github.com/activities/hello-world/
   - Keyword: Deutsch, Verwendung der Git ohne Kommandozeilen, Beginner

2. Title: **Git Cheat Sheet**

   - URL: https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf
   - Comment: GIT Cheat Sheet von GitHub
   - Keyword: Spickzettell

3. Title: **Pro Git book**

   - Autor: Scott Chacon and Ben Straub
   - URL: https://git-scm.com/book/en/v2
   - Keyword: Englisch, Advance, pdf
   
4. Title: **GIT-Tutorium Teil 1**

   - Autor: Sujeevan Vijayakumaran
   - Date: 12/2014
   - URL: http://www.freiesmagazin.de/mobil/freiesMagazin-2014-12-bilder.html#fm_14_12_git_teil1
   - Keyword: Deutsch, advance

5. Title: **GIT-Tutorium Teil 2**
   - Autor: Sujeevan Vijayakumaran
   - Date: 01/2015
   - URL: http://www.freiesmagazin.de/mobil/freiesMagazin-2015-01-bilder.html#fm_15_01_git_teil2
   - Keyword: Deutsch, advance
   
6. Title: **GIT-Tutorium Teil 3**
   - Autor: Sujeevan Vijayakumaran
   - Date: 02/2015
   - URL: http://www.freiesmagazin.de/mobil/freiesMagazin-2015-02-bilder.html#fm_15_02_git_teil3
   - Keyword: Deutsch, advance

7. Title: **Git Merge**
   - Autor: Webseite 04/2016
   - URL: https://www.atlassian.com/git/tutorials/using-branches/git-merge
   - Keyword: Englisch, beginner
   
# Video tutorials for Git/GitHub**. 

For some topics you can find some explanation videos around Git/GitHub on YouTube.
More helpful tutorials can be added here.
 
1. Title: **Lokale Repositories**
   - Author: The Morpheus Tutorials
   - Duration: 8:43 min
   - Date: 2017-01-31
   - URL: https://www.youtube.com/watch?v=9RbU-h0NH0A&list=PLNmsVeXQZj7rbmmqb1Lt_RGU4DEhelTrR&index=1
   - Keyword: Deutsch, beginner, repositories 
   
2. Title: **Branches, Merges, etc**
   - Autor: The Morpheus Tutorials
   - Duration: 10:06 min
   - Date: 2017-02-10
   - URL: https://www.youtube.com/watch?v=ZVoSBA03Tdc&list=PLNmsVeXQZj7rbmmqb1Lt_RGU4DEhelTrR&index=3
   - Keyword: Deutsch, beginner, branches 
   
3. Title: **Pull-Requests**
   - Autor: The Morpheus Tutorials
   - Duration: 10:16 min
   - Date: 2018-12-11
   - URL: https://www.youtube.com/watch?v=l8MZCnrSeQQ&list=PLNmsVeXQZj7rbmmqb1Lt_RGU4DEhelTrR&index=6
   - Keyword: Deutsch, beginner, pull
   
4. Title: **Issues**
   - Autor: The Morpheus Tutorials
   - Duration: 6:47 min
   - Date: 2018-12-13
   - URL: https://www.youtube.com/watch?v=wSHNvdRjB9Q&list=PLNmsVeXQZj7rbmmqb1Lt_RGU4DEhelTrR&index=8
   - Keyword: Deutsch, beginner, issues

5. Title: **Workflow**
   - Autor: Pilzschaf
   - Duration: 12:44 min
   - Date: 2016-10-08
   - URL: https://www.youtube.com/watch?v=hSbJaIdqwKg
   - Keyword: Deutsch, beginner, workflow
   
# Git GUI's

To visualize the Git repo and create the overview on the project, the following are the GUI of Git. (*** not recommended ***)

1. ** Sourcetree ** 
2. ** Git Extensions ** 
3. ** CodeReview **
4. ** GitBlade **
5. ** SmartGit **
6. ** ungit **
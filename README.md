# If you create NEW repo in remote side(GITHUB), want to create the same one in local-- use CLONE: 
1. under repo (topic) name, click 'clone and download'
2. copy SSH or HTTP link
3. open git.bash in PC
4. Choose which folder in which you want to add Cloned repo-- cloned repo will always be added to !!!current directory!!! in your local PC.
  
  -TO check current dir: open terminal, type 'pwd';
  
  -TO change current directory to where repo will be cloned and stored in, type cd [desired directory] You can type cd[space] and drag the desired directory folder to git bash terminal to avoid typing the directory
  
  -TO make a new dir where repo will be cloned and stored in, use mkdir

5. type 'git clone' then paste [SSH or HTTP link]
6. enter password--> then a folder named as repo name(e.g. hello-world) was added to the folder in Step 4 in your local PC. 

7. To dir to that repo, type 'cd hello-world'
    -then type 'start .'(win) or 'xdg-open .'(linux) to open folder in GUI format
    -OR type 'dir'(win) or 'ls'(linux) to list the items in this folder in terminal
    -To see the pathway of this folder: type 'cd'(win) or 'pwd'(linux)

-----------------

# How to check if the local has non-sync files compared to online github under same repository and push changes to update online github repo. That is when you create or edit the file locally under folder of repo, and want to sync changes online. 

NOTE: 

0. If you have changed remote side and local repo hasn't been synced yet, you need git pull to sync local with remote first (see next #), then go to step 0.1 below!!!!!!

0.1. cd [pathway to your repo directory in local PC]

0.2. Bypass large files before first time git commit/push: .gitignore  -> can create .gitignore file to ignore certain files/folders/file types (e.g. *.csv)
  - Github only can allow 100MB max per file to be git pushed to remote repo(github). 
  - Some local files like .csv files, .dat files, .zip files, ... are large sized files since they store large amount of data.
  - We usually ignore these types of files since if file size over limit above, git push will be rejected.
  - Method to realize above: using .gitignore, links: https://stackoverflow.com/questions/10744305/how-to-create-a-gitignore-file
  - .gitignore file example: https://coursework.vschool.io/create-a-gitignore/
1. check status: type 'git status'--> unsynced file will be marked as red
2. ADD:if want to add all unsynced file to online, type  'git add -A .' (then if you type git status again, there will be no red file)
3. COMMIT: add message to your commit: git commit -m "type your message here"
3.5 Undo last COMMIT: git reset HEAD^ --> return to untrack status (i.e. before "git add")
4. PUSH: type 'git push', then enter password as prompt. DONE! (desired file pushed and synced online)

-----------------

# When you have both online repo and local repo (same name), and you editted online one, how to sync changes local? i.e. how to let local repo pull changes from online github.
1. open terminal in the PC account (e.g. Windows IP or Ubuntu IP) where repo is located. 
2. type 'git pull

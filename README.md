# How-to-Clone-to-sync-with-local-PC
1. under repo (topic) name, click 'clone and download'
2. copy SSH link
3. open git.cmd in PC
4. type 'git clone' then paste SSH link
5. enter password--> folder named as file name(e.g. hello-world) was added to haiha folder

6. To confirm, type 'cd hello-world' to confirm direction to hello-world folder
7. type 'dir', can observe file pathway to that. DONE!

-----------------

# How to check if the local has non-sync files compared to online github under same repository. That is: you create or edit the file
under the folder of repo, and it needs to be sync to online.
0. type 'cd hello-world' to confirm direction to hello-world folder
1. check status: after direction of the pathway to folder of repo, type 'git status'--> unsynced file will be marked as red
2. ADD:if want to add all unsynced file to online, type  'git add -A .'
3. COMMIT: add message to your commit git commit -m "type your message here"
4. PUSH: type 'git push', then enter password as prompt. DONE! (desired file pushed and synced online)

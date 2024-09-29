# Making a remote github repository from a local git repository (using SSH)

Note that this is not the same as doing it with the https url, if you use https go to [the instructions for remote control with https](remotehttps.md). If you want to switch to SSH, go to [the instructions for setting up ssh](setupssh.md) first.

## How?
1. Make a new repository on Github. Don't add README.md if the local repository has any files.
2. Copy the SSH url from the github repository.
3. Make sure you're local file has .git, to do this in terminal (location: local repository) write:

   ```git init```
4. In terminal write (url is placeholder for the copied ssh url):
   
   ```git remote add origin url```
5. In terminal write ('main' is the name of the branch, change accordingly):

   ```git push -u origin main```
   
6. Do step 4 for each branch (make sure to work in the respective branch when writing the command). For example:

   ```git push -u origin secondbranch```

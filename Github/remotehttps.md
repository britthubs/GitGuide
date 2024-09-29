# Making a remote github repository from a local git repository (using https)

Note that this is not the same as doing it with the ssh url, if you use ssh go to [the instructions for remote control with ssh](remotessh.md). 
If you use https, but want to switch to SSH, go to the [instructions for setting up ssh](setupssh.md) first.

## How?

1. Make sure to have a personal access token generated and saved somewhere, the instructions to this can be found [here](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#using-a-personal-access-token-on-the-command-line).
2. Make a new repository on Github. Don't add README.md if the local repository has any files.
3. Copy the https url from the github repository.
4. Make sure your local file has .git, to do this in terminal (location: local repository) write:

   ```git init```
5. In terminal (location: local repository) write (url is the copied url from step 3):
   
   ```git remote add origin url```
   If you're asked to give a password, give the personal access token.
6. In terminal write ('main' is the name of the branch, change accordingly):

   ```git push -u origin main```
   If you're asked to give a password, give the personal access token.
   
7. Do step 5 for each branch (make sure to work in the respective branch when writing the command). For example:

   ```git push -u origin secondbranch```
   

# Making a remote github repository from a local git repository (using SSH)

## How?
1. Make a new repository on Github. Don't add README.md if the local repository has any files.
2. Copy the SSH url from the github repository.
3. In terminal (location: local repository) write:
   
   ```git remote add origin url```
4. In terminal write ('main' is the name of the branch, change accordingly):

   ```git push -u origin main```
   
6. Do step 4 for each branch (make sure to work in the respective branch when writing the command). For example:

   ```git push -u origin secondbranch```

# Changing from https to ssh to control remote repositories

## How?
1. Go to the local folder in the terminal and type the following:

   ```git remote -v```
   
   You will now see something along the lines like this (gitname is your account name
   and Repository is the name of your repository):
   ```
   origin	https://github.com/gitname/Repository.git (fetch)
   origin	https://github.com/gitname/Repository.git (push)
   ```
   This verifies you're using https to pull and push the contents of the project. If you are seeing something like the following,
   you are using ssh already and no further action is needed:

   ```
   origin	git@github.com:gitname/Repository.git (fetch)
   origin	git@github.com:gitname/Repository.git (push)
   ```
3. Copy the ssh url from the Github repository and type the following in terminal (pastethesshurlhere is a placeholder for the ssh url):

   ```
   git remote set-url origin pastethesshurlhere
   ```

4. To check, repeat step 1 and now you will see the following:
   
   ```
   origin	git@github.com:gitname/Repository.git (fetch)
   origin	git@github.com:gitname/Repository.git (push)
   ```

# Github Workflow Example

- We are simulating a Git-GitHub workflow here. First, let's create a new repository on GitHub called 'new-repo' (the name is not important). Alternatively, we can use an already existing repository on GitHub. 

- Check main/master?

- Now, let's check the Git configuration settings on our computer and make any necessary adjustments if there are areas that need to be corrected.

- If we didn't have authentication, we should have an access token or we can use other methods to authenticate

´´´bash 
git config --list
git config user.name
git config user.email
´´´

- Clone the repository to local

´´´bash 
git clone https://github.com/xxxxxx/new-repo.git
´´´

- cd into repository 

´´´bash 
cd new-repo
´´´
- We should check if there is a correct connection between the local and remote repositories when using a repository for the first time.

´´´bash 
git remote -v
´´´

- Don't hesitate to enter these three commands every time.

´´´bash 
git status
git log
git branch
´´´

- Add our first file and check our connection to remote / create a file called .gitignore and push ...

´´´bash
touch .gitignore 
git add .
git commit -m "initial commit"
git push -u origin main 
´´´

- When working with Git/GitHub, we should not work in the main (master) branch, so let's create a branch and switch into it.

´´´bash 
git checkout -b feature/test
git branch
´´´

- Now let's create a README.md file and write something, and if it already exists, we can make a change inside it. And of course check status/branch/log 

´´´bash 
touch README.md
git branch
git status
git log
´´´
- Now it's time to see the changes we have made. (all changes or file spesifik changes)

´´´bash 
git diff
git diff README.md
´´´

- Now send our changes to the staging area

´´´bash 
git add .
´´´

or 

´´´bash 
git diff README.md
´´´

- As always

´´´bash 
git branch
git status
git log

´´´
- Yes committing our changes 

´´´bash 
git commit -m "change README file"
git status
git log
´´´

- Now we saw a new log / a new commit

- It's time to send from local to remote

´´´bash 
git push -u origin feature/test
git branch
git log
git checkout main
git log
git status
´´´

- Go to Github and see your newly created branch

- Again check logs on local and compare with remote commit ID

- The "git fetch" command retrieves all changes and information from the remote repository to the local repository, but does not modify your current working files.

´´´bash 
git log
git fetch
git log
git pull
git log
git branch
´´´
- The "git pull" command fetches changes from the remote repository to the local repository and updates your current working files with these changes.

- Compare local and remote 'main', if they are on same 'commit id' we can delete branch

´´´bash 
git branch-d feature/test
´´´

# Best Practices for Working with Git and GitHub

- Always commit with meaningful messages: When working with Git and GitHub, it's important to use clear and descriptive commit messages to explain what changes have been made and why.

- Keep your branches organized: Maintain a clear branch strategy and naming convention to keep your repository organized and understandable for all contributors.

- Regularly push your local commits to remote: Regularly pushing your commits to the remote repository ensures that your changes are safely stored and accessible to other team members.

- Use pull requests for merging: Utilize pull requests for code reviews and discussions before merging changes, enhancing collaboration and code quality.

- Keep your repository updated: Frequently pull changes from the remote repository to your local repository to stay updated with the latest developments and avoid merge conflicts.
# DevOpsExample

echo "# DevOpsExample" >> README.md
git init
git add README.md
Or simply: git add . (I think the '.' period symbol is a wildcard for all files)
git commit -m "first commit"
git remote add origin https://github.com/lynstanford/DevOpsExample.git
git push -u origin master

# Once in App Center, make changes to Build Configuration default (master) branch:
  Build app
  Project: Project(csproj)  / Solution file(sln)
  Configuration: Debug / Release
  SDK version: Language for OS
  OS Version: Alpha, Beta etc
  Build type: Device build / Simulator build*
  Build frequency: build this branch on every push*
  Click Save - this configures CI for your OS application.

# In a Terminal
Navigate to directory containing app 'csproj', or 'sln' file - e.g. C:\Users\my_name\DevOpsExample\my_project.csproj
~$ git checkout -b newbranch1

This creates a new branch name called 'newbranch1'
Any new changes in VS or VS Code will only be made in the new branch (they won't affect the master branch)
~$ git commit -am "newbranch1 is ready"

To update your commit comment or description
~$ git push origin newbranch1

This will contain all the changes in both the 'master' and 'newbranch1' which can be checked in GitHub repository
In GitHub click 'Compare & Pull Request' button on the right
This will create a pull request to merge into the master branch
Click 'Create Pull Request'

Under the 'Checks' tab you will see you are waiting for your builds to take place before they're added to the master
These builds should be triggered when the Pull Requests are created
When both checks are complete - Merge Pull Request

Can delete the newbranch1 branch and hopefully your master branch gets updated automatically with new code

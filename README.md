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

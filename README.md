#The "Right Way" to Create a New Repo

When I was a budding developer there were a few occassions where I created a repo on my local machine, then created a repo on GitHub, cloned it to my local machine, and wondered why I couldn't connect the two, or why I had a directory of the same name inside of itself. To help you eliminate this problem and get going faster on your project, here are some very helpful, sequential, steps to set you out on the right foot. 

##What You Will Need
* a GitHub account
* the command line (these instructions are written for Mac's Terminal application)

##Steps
1. Open the command line ([command]+[spacebar]+type "terminal") and `cd` into the project directory.
  1. To create a new directory: `mkdir /path/to/directory/name && cd "$_"`
  2. RECOMMENDED: Create a main workspace directory wherein all of your projects and repos will live.
2. Initialize the local project as a Git repository: `git init`

   NOTICE: At this point you are working on an "unborn branch". To create the master branch you need to make your first commit.

   OPTIONAL: Create any file such as index.html or README.md using the command `touch index.html`
3. Stage all your files for commit with  `git add .` (the `.` means "everything")

   To stage only one file or multiple files use `git add file1.ext file2.ext`

   To unstage a file, use `git reset HEAD your-file.ext` 
4. Commit changes to the current branch with `git commit -m "initial commit"`

   Your very first commit creates the master branch. Prior to this you HEAD and master are the same "thing".
5. Now go to your GitHub account.
6. Create a new repository. 

   Do not initialize with a README. 

   Do not add a .gitignore or a license.
7. On the screen that loads after creating your GitHub repo find the instructions for pushing an existing repository from the command line.

   You should be instructed to enter the following:

   `git remote add origin YOUR REMOTE REPOSITORY URL`

   >Sets the remote repo for pushing and pulling.

   `git remote -v`

   >Verifies the new remote URL. Make sure this verified URL matches the one for your GitHub repo.

   `git push -u origin master`

   >Pushes your saved commit to your repo on GitHub.

8. Now that you have your local and remote repositories setup and connected, its time to take a look at some best practices for developing. This is especially important for developing projects with other human beings. 

   [Click here for "A Successful Git Branching Model" by Vincent Driessen](http://nvie.com/posts/a-successful-git-branching-model/)



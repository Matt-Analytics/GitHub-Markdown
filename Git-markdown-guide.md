# Git & GitHub

## What is version control?

Some of the key points of version control are:

- Keeps track of changes made to files via version history
- Enables collaboration on files in the same project
- Allows for reverting to previous versions of a project/file
- Aids in avoiding conflicts when sharing work

## Git

### What is Git?

Some key aspects of Git are:
- An open source version control system
- Allows for project contributors to have local copies of projects
- Provides the ability to view and track version history and make changes
- Utilises a command-line user interface called Git Bash
- A directory/folder within Git is called a "repository" or "repo"

### How do you use Git?
The steps for downloading, installing and setting up Git are:

1. **Download Git:**
   - Visit the official Git website: [https://git-scm.com/downloads](https://git-scm.com/downloads)
   - The website will automatically detect your operating system and offer the appropriate download

2. **Run the Installer:**
   - Once the download is complete, open the installer
   - Follow the installation prompts

3. **Configure Git:**
    - Open Git Bash and set your name and email:
   ```bash
     git config --global user.name "Your Name"
   
     git config --global user.email "your.email@example.com"
     ```
   - To change the default branch using Git Bash:
   ```bash
     git config --global init.defaultbranch main
     ```

### How to create a Git repository
To create a new repository using Git, follow these steps:
- Open the Git Bash terminal and create the directory you wish to use, then switch to it
    ```bash
     mkdir path/to/your/project
  
     cd path/to/your/project
     ```
- Create the Git repository, and you will have a `.git` file in your project folder:
    ```bash
     git init
     ```
- You now have a git repository!


It is good practice to create a `.gitignore` file to exclude certain file types from being tracked:
  ```bash
     notepad .gitignore
  ```
This will open a notepad instance where you can write any type of file to be ignored by Git
```text
   #Exclude files of the following type:
   *.properties
```

### Staging and Committing to a Git repository

To make changes to your project, you must track them and commit them. These are the steps to do so:

Before committing changes, you first stage them:

- To see which files have been modified or added, use:
  ```bash
  git status
  ```

- To stage a file you can use the `git add` command. Here we create a README markdown file and stage it
    ```bash
    notepad README.md
    
    git add README.md
    ```
To commit to the repository with a message:

  ```bash
    git commit -m "First Commit"
  ```

To commit all items in staging with a message to the repository you can use:

 ```bash
    git commit -a -m "Commit all"
  ```
  
To compare the working directory, staging area, and your latest commit you can use:

```bash
    git diff
  ```
Finally, to display a list of commits we can use the following command:

```bash
    git log
  ```

## GitHub

### What is GitHub?

GitHub is an online service for hosting and managing Git repositories.

Some key features are:
- Allows for storing and managing code online, making it accessible anywhere
- Enables collaboration between multiple users on the same project
- GitHub is built on top of Git, meaning it has the same version control capabilities
- Pull requests are used to propose any changes to the repository

### GitHub Account

To create a GitHub account you can simply visit the website and sign up via email.

- Via your browser go to [https://github.com](https://github.com)
- Go to the **Sign up** button and input an email, username, and password and complete any security checks
- Finalise the process by verifying your email address and done!

### Creating a remote repository

- Once logged in, click the **+** in the top right corner and select **New repository**
- Now fill in details like repository name, public or private, etc.
- Finally, click **Create repository**

### How to copy a local repository to GitHub
- After clicking **Create repository** in the previous step, a quick setup should appear
- Make sure  the link in the quick setup has https enabled
- Go back to Git Bash on your local machine and type the following command:
  ```bash
    git remote add origin https://github.com/Account/GitExample.git
  ```
- To push our local main branch to the remote one we use the following command:
  ```bash
      git push origin main
  ```
- The previous step will require the user to insert either login details or a GitHub token

### How to clone a remote Github repository to your local machine

- Firstly, ensure you change to your user directory by using the `cd` command itself
- Then to clone your GitHub repository, click the **<> Code** button on your repository page and copy the link
- To clone the remote repository, type the following in Git Bash:
  ```bash
      git clone https://github.com/Account/GitExample.git
  ```

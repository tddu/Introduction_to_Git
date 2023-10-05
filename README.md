
# Introduction to Git, GitHub, and GitHub Desktop

## Part 1: Basics of Git and GitHub

### Table of Contents
1. [Introduction](#introduction)
2. [Requirements & Setup](#requirements--setup)
3. [Basic Git Commands](#basic-git-commands)
4. [Branching in Git](#branching-in-git)
5. [Merging and Conflict Resolution](#merging-and-conflict-resolution)

### Introduction

Git is a distributed version control system, enabling users to track and manage code changes. GitHub is a platform that uses Git to provide cloud-based hosting for repositories, promoting collaboration and version control on shared projects.

This section provides a basic introduction to Git and GitHub. It's designed for beginners and will give you an understanding of the essential concepts and commands.

### Requirements & Setup

Before diving in, ensure you have met all the prerequisites:

- **Git Installation**: Depending on your OS, [Windows](#windows), [Mac OS X](#macos), or [Linux](#linux), follow the respective links to install Git.
- **Text Editors**: Use a plain text editor like [VS Code](https://code.visualstudio.com/) for editing and viewing files.
- **Setting Up Git**:
  ```bash
  $ git config --global user.name "Your Name"
  $ git config --global user.email your.email@example.com
  ```

### Basic Git Commands

1. **Initialization & Cloning**:
    - Start a new repository or obtain one from an existing URL.
      ```bash
      $ git init
      $ git clone [repository_url]
      ```

2. **Tracking Changes**:
    - View the status of your files in the working directory and staging area.
      ```bash
      $ git status
      ```

    - Add changes in your working directory to the staging area.
      ```bash
      $ git add [filename(s)]
      ```

    - Commit changes from the staging area to the repository.
      ```bash
      $ git commit -m "Your meaningful message here"
      ```

3. **Branching and Switching**:
    - View all branches in your repository.
      ```bash
      $ git branch
      ```

    - Create a new branch or switch to an existing one.
      ```bash
      $ git checkout -b [branch_name]
      $ git checkout [existing_branch_name]
      ```

4. **Remote Repositories**:
    - Push or pull your commits to a remote repository.
      ```bash
      $ git push
      $ git pull
      ```

### Branching in Git

Branching allows multiple lines of development to take place concurrently within a repository. This section focuses on how to create, switch, and manage branches.

1. **Creating a Branch**:  
    ```bash
    $ git checkout -b [branch_name]
    ```

2. **Switching Between Branches**:  
    ```bash
    $ git checkout [branch_name]
    ```

3. **Listing All Branches**:  
    ```bash
    $ git branch
    ```

### Merging and Conflict Resolution

Merging integrates changes from one branch into another. If changes conflict, you'll need to resolve them.

1. **Merging a Branch**:  
    ```bash
    $ git merge [source_branch_name]
    ```

2. **Resolving Conflicts**: In case of conflicts, open the conflicted file and manually resolve the differences. After resolving, mark the file as merged:
    ```bash
    $ git add [resolved_filename]
    ```

3. **Completing the Merge**: Once all conflicts are resolved, commit the changes to finalize the merge:
    ```bash
    $ git commit -m "Resolved merge conflicts"
    ```

---


## Part 2: Advanced Git Features and Introduction to GitHub Desktop

### Table of Contents
1. [Advanced Git Features](#advanced-git-features)
2. [GitHub Desktop](#github-desktop)
3. [Setting up and Using GitHub Desktop](#setting-up-and-using-github-desktop)
4. [Conclusion & Further Reading](#conclusion--further-reading)

### Advanced Git Features

#### 1. **Git Stash**: 
Temporarily saves changes that are not yet ready for a commit.
   - **Stashing changes**:
     ![Git Stash](https://example.com/images/git-stash.png)
     ```bash
     $ git stash
     ```

   - **Applying stashed changes**:
     ```bash
     $ git stash apply
     ```

#### 2. **Git Rebase**: 
Reapply commits on top of another branch.
   - **Rebasing**:
     ![Git Rebase](https://example.com/images/git-rebase.png)
     ```bash
     $ git rebase [base_branch_name]
     ```

#### 3. **Git Cherry-Pick**: 
Selectively apply commits from one branch onto another.
   - **Cherry-picking a commit**:
     ![Git Cherry-Pick](https://example.com/images/git-cherry-pick.png)
     ```bash
     $ git cherry-pick [commit_hash]
     ```

### GitHub Desktop

GitHub Desktop is a GUI (Graphical User Interface) for managing your Git repositories. This provides an alternative to using the command line and simplifies tasks like committing, branching, and merging.

![GitHub Desktop Interface](https://example.com/images/github-desktop-interface.png)

### Setting up and Using GitHub Desktop

1. **Installation**:
    - Download and install GitHub Desktop from [the official website](https://desktop.github.com/).
      ![GitHub Desktop Download](https://example.com/images/github-desktop-download.png)

2. **Setting Up**:
    - Open the application and log in using your GitHub account.
    - Configure your commit details (name & email).
      ![GitHub Desktop Setup](https://example.com/images/github-desktop-setup.png)

3. **Using GitHub Desktop**:
    - **Clone a Repository**: Use the `File > Clone Repository` option.
      ![Clone Repository](https://example.com/images/clone-repo.png)

    - **Make Changes**: Edit your files and see the changes reflected in the app.
    - **Commit Changes**: Add a commit message and description, then click `Commit`.
      ![Commit Changes](https://example.com/images/commit-changes.png)

    - **Push & Pull**: Sync your local changes with the remote repository.
      ![Push and Pull](https://example.com/images/push-pull.png)

### Conclusion & Further Reading

Congratulations on diving deeper into Git and getting introduced to GitHub Desktop! By mastering these tools, you're on your way to efficient and collaborative coding.

For those interested in pushing their Git skills even further, consider exploring more about:
- [Interactive Rebasing](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History)
- [Advanced Merging](https://git-scm.com/docs/git-merge)
- [In-depth GitHub Desktop](https://docs.github.com/en/desktop)

---

# Introduction to Git, GitHub, and GitHub Desktop

## Part 3: Collaborative Work and Advanced GitHub Features

### Table of Contents
1. [Working Collaboratively](#working-collaboratively)
2. [Advanced GitHub Features](#advanced-github-features)
3. [GitHub Pages and GitHub Actions](#github-pages-and-github-actions)
4. [Conclusion & Next Steps](#conclusion--next-steps)

### Working Collaboratively

#### 1. **Forking a Repository**:
A fork is a copy of a repository, allowing you to make changes without affecting the original project.
   - **Creating a fork**:
     ![Forking a Repository](https://example.com/images/github-fork.png)
     ```bash
     [Click on the 'Fork' button at the top-right of the repository page]
     ```

#### 2. **Creating Pull Requests**:
A pull request (PR) lets you propose changes to a repository, promoting code review and collaboration.
   - **Opening a pull request**:
     ![Creating a Pull Request](https://example.com/images/github-pull-request.png)
     ```bash
     [Make changes in your fork > Click 'New Pull Request' in the original repository]
     ```

#### 3. **Merging Pull Requests**:
Accept proposed changes into the main codebase.
   - **Merging a PR**:
     ![Merging a Pull Request](https://example.com/images/github-merge-pr.png)
     ```bash
     [Review the PR > Click 'Merge Pull Request']
     ```

### Advanced GitHub Features

#### 1. **GitHub Issues**:
Used to track ideas, enhancements, tasks, and bugs for work on GitHub.
   - **Opening an issue**:
     ![GitHub Issues](https://example.com/images/github-issues.png)
     ```bash
     [Navigate to 'Issues' tab > Click 'New Issue']
     ```

#### 2. **GitHub Projects**:
Project boards on GitHub help you organize and prioritize your work.
   - **Creating a project board**:
     ![GitHub Projects](https://example.com/images/github-projects.png)
     ```bash
     [Navigate to 'Projects' tab > Click 'New Project']
     ```

### GitHub Pages and GitHub Actions

#### 1. **GitHub Pages**:
Host static websites directly from your GitHub repository.
   - **Setting up GitHub Pages**:
     ![GitHub Pages](https://example.com/images/github-pages.png)
     ```bash
     [Repository Settings > GitHub Pages section > Select branch and folder]
     ```

#### 2. **GitHub Actions**:
Automate workflows, from software builds to deployments and more.
   - **Creating a new workflow**:
     ![GitHub Actions](https://example.com/images/github-actions.png)
     ```bash
     [Navigate to 'Actions' tab > Set up a workflow yourself or choose from marketplace templates]
     ```

### Conclusion & Next Steps

Collaborative work on GitHub involves various tools and practices to ensure code integrity and effective team dynamics. By mastering the features discussed, you're better equipped to contribute to open-source projects or work collaboratively on private ventures.

As next steps, consider:
- Exploring [GitHub Marketplace](https://github.com/marketplace) for apps and actions that enhance your workflow.
- Delving into [Advanced Git Techniques](https://git-scm.com/book/en/v2) for complex project scenarios.
- Joining communities like [GitHub Stars](https://stars.github.com/) or [GitHub Sponsors](https://github.com/sponsors) for further engagement.

Remember, the journey of mastering Git and GitHub is continuous, so keep experimenting, learning, and sharing with the community!


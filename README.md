## Git Tutorial: Handling Merges, Rebases, and Pull Requests

### Prerequisites:

- Basic knowledge of Git commands.
- A GitHub account.

### Objective:

By the end of this tutorial, you should be able to:

1. Clone a repository.
2. Make changes and push them.
3. Resolve merge conflicts.
4. Use the rebase command.
5. Raise a pull request (PR).

### Let's Get Started!

#### 1. Clone the Repository:

Start by cloning the existing repository. This repository is located on a remote server, which is typically GitHub for most projects. By cloning it, you create a local copy on your machine which you can edit and push back to the remote repository.

```bash
$ git clone https://github.com/Waseem0912-coder/Introduction_to_Git
```

#### 2. Create a New Branch:

To avoid conflicts with the main codebase, always work on a new branch.

```bash
$ git checkout -b [your_name]-choice
```

Replace `[your_name]` with your actual name.

#### 3. Choose Your Greek God:

Open the provided text file in the repository. Choose one Greek god from the following list and add it to the file:

- Zeus
- Hera
- Poseidon
- Demeter
- Athena
- Apollo
- Artemis
- Ares
- Aphrodite
- Hephaestus
- Hermes
- Dionysus

Save and close the file.

#### 4. Commit and Push:

Commit your changes and push them to your branch on the remote GitHub repository.

```bash
$ git add .
$ git commit -m "Chose my Greek god"
$ git push origin [your_name]-choice
```

#### 5. Rebase:

Before raising a PR, ensure your branch has the latest changes from the main branch of the remote repository. Rebasing allows you to apply your changes on top of the latest changes in the main branch.

```bash
$ git checkout main
$ git pull origin main
$ git checkout [your_name]-choice
$ git rebase main
```

If you encounter conflicts during the rebase (which is expected given the Greek god choice), proceed to step 6. If not, move on to step 7.

#### 6. Resolve Merge Conflicts:

Multiple students might have chosen the same Greek god, leading to a merge conflict.

Open the text file, and you'll see conflict markers:

```
<<<<<<< HEAD
Apollo
=======
Athena
>>>>>>> [commit_hash]
```

To resolve this:

1. Decide which choice to keep or combine them.
2. Remove the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
3. Save the file.

After resolving all conflicts:

```bash
$ git add .
$ git rebase --continue
```

If more conflicts arise, resolve them. Once there are no more conflicts, the rebase will conclude.

#### 7. Raise a Pull Request:

Now, return to the GitHub repository online:

1. Click on "Pull Requests".
2. Select "New Pull Request".
3. For the base branch, choose "main". For the compare branch, pick your branch (`[your_name]-choice`).
4. Review your changes and click "Create Pull Request".
5. Add a title and description for your PR and submit.

---

Congratulations! You've now tackled changes, navigated conflicts, and initiated a PR. Handling merge conflicts can seem daunting at first, but with practice, it becomes intuitive. This exercise imparts the collaborative flow of team projects using Git and GitHub, enhancing your version control skills.

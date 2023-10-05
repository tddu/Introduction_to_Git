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

First, let's start by cloning the existing repository. 

```bash
$ git clone [repository_url] 
```

Replace `[repository_url]` with the URL of the repository you want to clone. This will create a local copy on your machine.

#### 2. Create a New Branch:

Always work on a new branch to avoid conflicts with the main codebase. 

```bash
$ git checkout -b [your_name]-favorite-pokemon
```

Replace `[your_name]` with your actual name.

#### 3. Add Your Favorite Pokémon:

Open the provided text file in the repository. Add your name and your favorite Pokémon. Save and close the file.

For example:
```
John: Charizard
```

#### 4. Commit and Push:

Commit your changes and push them to your branch on GitHub.

```bash
$ git add .
$ git commit -m "Added my favorite Pokémon"
$ git push origin [your_name]-favorite-pokemon
```

#### 5. Rebase:

Before raising a PR, ensure your branch has the latest changes from the main branch.

```bash
$ git checkout main
$ git pull origin main
$ git checkout [your_name]-favorite-pokemon
$ git rebase main
```

If you encounter conflicts during the rebase, skip to step 6. If not, move on to step 7.

#### 6. Resolve Merge Conflicts:

If multiple students have modified the same lines in the text file, you'll encounter a merge conflict.

Open the text file and you'll see something like:

```
<<<<<<< HEAD
John: Charizard
=======
Jane: Bulbasaur
>>>>>>> [commit_hash]
```

To resolve this:

1. Decide which changes to keep.
2. Remove the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
3. Save the file.

After resolving all conflicts:

```bash
$ git add .
$ git rebase --continue
```

If there are more conflicts, resolve them. If not, the rebase will complete.

#### 7. Raise a Pull Request:

Go to the repository on GitHub.

1. Click on "Pull Requests".
2. Click "New Pull Request".
3. For the base branch, choose "main". For the compare branch, choose your branch (`[your_name]-favorite-pokemon`).
4. Review your changes and click "Create Pull Request".
5. Add a title and description for your PR and submit.

---

That's it! You've now made changes, resolved conflicts, and raised a PR. Remember, handling merge conflicts can be tricky, but with practice, it becomes easier. This exercise will help you understand the flow of working collaboratively in a team using Git and GitHub.

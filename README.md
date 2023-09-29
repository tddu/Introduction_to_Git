
## Introduction to Git and Github



## Table of Contents

* [Introduction](#introduction)
* [Class Requirements](#Class-requirements)
* [Text Editors](#text-editors)
* [Installing Git](#installing-git)
* [Seeking Help](#seeking-help)


Introduction
----

Git is a system for managing snapshots of plain text projects.
It is widely used in industry and academia for distributed collaboration amongst programmers.
It is also useful to individuals who want to manage and back up plain text projects across multiple devices.
GitHub is a popular website for hosting projects that use Git.

This class will provide a gentle introduction to Git and GitHub aimed at a general audience.
Since Git is most often used in a text-based environment,
we will also cover some simple use of the Unix command line.
The goal of the class is that you will attain some idea of what Git is and how to begin using it.


Requirements
----

It is easy for a class to get derailed by finicky technical issues caused by operating system differences or internet connection problems.
You have some responsibility for ensuring you meet the class requirements.

Please do the right thing by other students:

**You must have all software installed and an internet connection established before the class begins.**

### Required Software

You will need software for editing plain text files and for using Git.
More detailed software suggestions and instructions are below.

You must have the software downloaded before the class.

You should also do some basic sanity checks to ensure that it works correctly.
At a minimum, you must be able to open a terminal and run `git --version` without seeing any errors.
You must also be able to edit plain text files.


Text Editors
----

The class will require you to have access to a _plain text editor_.
Some common text editors include Notepad, Eclipse, Atom, Vim and Emacs.
Some text editors are easier to use than others,
and some offer more features.

Notepad is easy to use but has minimal features.
Vim and Emacs are hard for beginners to use, but they become more and more powerful with experience.

For this class, we recommend [VS Code](https://code.visualstudio.com/).

VS Code is a free and cross platform text editor.
It looks very pretty, it is very customizable with a lot of features and plugins available,
it is easy to install, and it will work on everyone's laptop.
You will be able to keep using it after the class is over, forever, without paying anything.

If you already have some other preferred text editor,
you may choose to use that in the class.
However, if you run into problems, it is possible that no one will know how to help you.
Furthermore, you might take class time away from the intended material,
which is not fair on other attendees.

So, only use an alternative text editor if you feel confident that you can solve any problems that could arise.

**Note:** Do _not_ use a product such as Microsoft Word.
A word processor is not the same as a text editor.
The distinction will be explored in more detail in the class itself.


# Installing Git

Although Git is cross platform,
each operating system offers different installation methods.
We are still evaluating which methods will be optimal for our class.

Have a look through the available options and choose one that seems suitable to you.
You may need to try more than one to find a good fit for you and your system.

* [Windows](#windows)
* [Mac OS X](#mac)
* [Linux](#linux)


# Windows

There are two  main ways to install Git in Windows,
depending on which version of Windows you are running.


#### Git for Windows

This is the easiest but least powerful method.
Download the installer from https://git-scm.com/download/win and run it.



# Download for Linux and Unix

It is easiest to install Git on Linux using the preferred package manager of your Linux distribution. If you prefer to build from source, you can find tarballs  [on kernel.org](https://www.kernel.org/pub/software/scm/git/). The latest version is  [2.42.0](https://www.kernel.org/pub/software/scm/git/git-2.42.0.tar.gz).

### Debian/Ubuntu

For the latest stable version for your release of Debian/Ubuntu

`# apt-get install git`

For Ubuntu, this PPA provides the latest stable upstream Git version

`# add-apt-repository ppa:git-core/ppa`  `# apt update; apt install git`

### Fedora

`# yum install git` (up to Fedora 21)  
`# dnf install git` (Fedora 22 and later)

### Gentoo

`# emerge --ask --verbose dev-vcs/git`

### Arch Linux

`# pacman -S git`

### openSUSE

`# zypper install git`

### Mageia

`# urpmi git`

### Nix/NixOS

`# nix-env -i git`

### FreeBSD

`# pkg install git`

### Solaris 9/10/11 ([OpenCSW](https://www.opencsw.org/))

`# pkgutil -i git`

### Solaris 11 Express

`# pkg install developer/versioning/git`

### OpenBSD

`# pkg_add git`

### Alpine

`$ apk add git`

### Red Hat Enterprise Linux, Oracle Linux, CentOS, Scientific Linux, et al.

RHEL and derivatives typically ship older versions of git. You can  [download a tarball](https://www.kernel.org/pub/software/scm/git/)  and build from source, or use a 3rd-party repository such as  [the IUS Community Project](https://ius.io/)  to obtain a more recent version of git.

### Slitaz

`$ tazpkg get-install git`



# Download for macOS

There are several options for installing Git on macOS. Note that any non-source distributions are provided by third parties, and may not be up to date with the latest source release.

**Choose one of the following options for installing Git on macOS:**

### Homebrew

Install  [homebrew](https://brew.sh/)  if you don't already have it, then:  
`$ brew install git`

### MacPorts

Install  [MacPorts](https://www.macports.org/)  if you don't already have it, then:  
`$ sudo port install git`

### Xcode

Apple ships a binary package of Git with  [Xcode](https://developer.apple.com/xcode/).

### Binary installer

Tim Harper provides an  [installer](https://sourceforge.net/projects/git-osx-installer/)  for Git. The latest version is  [2.33.0](https://sourceforge.net/projects/git-osx-installer/files/git-2.33.0-intel-universal-mavericks.dmg/download?use_mirror=autoselect), which was released about 2 years ago, on 2021-08-30.

### Building from Source

If you prefer to build from source, you can find tarballs  [on kernel.org](https://www.kernel.org/pub/software/scm/git/). The latest version is  [2.42.0](https://www.kernel.org/pub/software/scm/git/git-2.42.0.tar.gz).

### Installing git-gui

If you would like to install  [git-gui](https://git-scm.com/docs/git-gui/)  and  [gitk](https://git-scm.com/docs/gitk/), git's commit GUI and interactive history browser, you can do so using  [homebrew](https://brew.sh/)  
`$ brew install git-gui`


# Setup

First thing to do is to setup your identity. This identifies you to
other people who download the project.

    $ git config --global user.name "Your Name"
    $ git config --global user.email your.email@example.com

As a helpful step, you may want to set Git to use your favourite editor

    $ git config --global core.editor vim

# Starting your journey

First, clone this repository:

    $ git clone https://github.com/Waseem0912-coder/git-workshop.git

You may want to fork (create your own copy of) the project on github and
clone from your own repo. You can find the fork button at the top right of
the screen on a github repository, or more help about doing that [here](https://help.github.com/articles/fork-a-repo/).

Once you have cloned your repository, you should now see a directory
called `git-workshop`. This is your `working directory`

    $ cd git-workshop
    $ ls

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Help-browser.svg/20px-Help-browser.svg.png)
Stuck? Ask for help from the TA

If you are curious, you should also see the `.git` subdirectory. This is
where all your repository’s data and history is kept.

    $ ls -a .git

You will see :

    branches  config  description  HEAD  hooks  info  objects  refs

# The staging area

Now, let’s try adding some files into the project. Create a couple of
files.

Let’s create two files named `bob.txt` and `alice.txt`.

    $ touch alice.txt bob.txt

Let’s use a mail analogy.

In Git, you first add content to the `staging area` by using `git add`.
This is like putting the stuff you want to send into a cardboard box.
You finalize the process and record it into the git index by using
`git commit`. This is like sealing the box - it’s now ready to send.

Let’s add the files to the staging area

    $ git add alice.txt bob.txt

# Committing

You are now ready to commit. The `-m` flag allows you to enter a message
to go with the commit at the same time.

    $ git commit -m "I am adding two new files"

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Help-browser.svg/20px-Help-browser.svg.png)
Stuck? Ask for help from the workshop staff

# Let’s see what just happened

We should now have a new commit. To see all the commits so far, use
`git log`

    $ git log

The log should show all commits listed from most recent first to least
recent. You would see various information like the name of the author,
the date it was commited, a commit SHA number, and the message for the
commit.

You should also see your most recent commit, where you added the two new
files in the previous section. However git log does not show the files
involved in each commit. To view more information about a commit, use
`git show`.

    $ git show

You should see something similar to:

    commit 5a1fad96c8584b2c194c229de7e112e4c84e5089
    Author: Waseem0912-coder
    Date:   Fri Sept 29 19:13:42 2011 +1200

        I am adding two new files

    diff --git a/alice.txt b/alice.txt
    new file mode 100644
    index 0000000..e69de29
    diff --git a/bob.txt b/bob.txt
    new file mode 100644
    index 0000000..e69de29

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Help-browser.svg/20px-Help-browser.svg.png)
Stuck? Ask for help from the workshop staff

# A necessary digression

In this section, we are going to add more changes, and try to recover
from mistakes.

Be forewarned, this next step is going to be hard. We will need to add
some content to alice.txt.

Open `alice.txt` and type in your favourite line from a song, or:

e.g. Lorem ipsum Sed ut perspiciatis, unde omnis iste natus error sit
voluptatem accusantium doloremque laudantium

Then **save** the file

What did we change? A very useful command is `git diff`. This is very
useful to see exactly what changes you have done.

    $ git diff

You should see something like the following:

    diff --git a/alice.txt b/alice.txt
    index e69de29..2aedcab 100644
    --- a/alice.txt
    +++ b/alice.txt
    @@ -0,0 +1 @@
    +Lorem ipsum Sed ut perspiciatis, unde omnis iste natus error sit voluptatem accusantium doloremque laudantium

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Help-browser.svg/20px-Help-browser.svg.png)
Stuck? Ask for help from the class staff

# Staging area again

Now let’s add our modified file, `alice.txt` to the staging area. Do you
remember how ?

Next, check the `status` of `alice.txt`. Is it in the staging area now?

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Help-browser.svg/20px-Help-browser.svg.png)
Stuck? Ask for help from the class staff

# Undoing

Let’s say we did not like putting Lorem ipsum into `alice.txt`. One
advantage of a staging area is to enable us to back out before we
commit - which is a bit harder to back out of. Remembering the mail
analogy - it’s easier to take mail out of the cardboard box before you
seal it than after.

Here’s how to back out of the staging area :

    $ git reset HEAD alice.txt

    Unstaged changes after reset:
    M   alice.txt

Compare the `git status` now to the git status from the previous
section. How does it differ?

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Help-browser.svg/20px-Help-browser.svg.png)
Stuck? Ask for help from the class staff

Your staging area should now be empty. What’s happened to the Lorem
Ipsum changes? It’s still there. We are now back to the state just
before we added this file to staging area. Going back to the mail
analogy, we just took our letter out of the box.

# Undoing II

Sometimes we did not like what we have done and we wish to go back to
the last *recorded* state. In this case, we wish to go back to the state
just before we added the Lorrem ipsum text to `alice.txt`.

To accomplish this, we use `git checkout`, like so:

    $ git checkout alice.txt

You have now un-done your changes. Your file is now empty.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Help-browser.svg/20px-Help-browser.svg.png)
Stuck? Ask for help from the class staff

# Branching

Most large code bases have at least two branches - a ‘live’ branch and a
‘development’ branch. The live branch is code which is OK to be deployed
on to a website, or downloaded by customers. The development branch
allows developers to work on features which might not be bug free. Only
once everyone is happy with the development branch would it be merged
with the live branch.

Creating a branch in Git is easy. The `git branch` command, when used by
itself, will list the branches you currently have

    $ git branch

The `*` should indicate the current branch you are on, which is
`master`.

If you wish to start another branch, use
`git checkout -b (new-branch-name)` :

    $ git checkout -b exp1

Try git branch again to check which branch you are currently on:

    $ git branch
      exp1
    * master

The new branch is now created. Now let’s work in that branch. To switch
to the new branch:

    $ git checkout exp1

`git checkout (branch-name)` is used to switch branches.

Let’s perform some commits now,

    $ echo 'some content' > test.txt
    $ git add test.txt
    $ git commit -m "Added experimental txt"

Now, let’s compare them to the master branch. Use `git diff`

    $ git diff master

Basically what the above output says is that `test.txt` is present on
the `exp1` branch, but is absent on the `master` branch.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Help-browser.svg/20px-Help-browser.svg.png)
Stuck? Ask for help from the TA 

# Now you see me, now you don’t

Git is good enough to handle your files when you switch between
branches. Switch back to the `master` branch

Try switching back to the master branch (Hint: It’s the same command we
used to switch to the exp1 branch above)

Now, where’s our `test.txt` file ?

    $ ls
    README.textile  alice.txt   bob.txt     gamow.txt

As you can see the new file you created in the other branch has
disappeared. Not to worry, it is safely tucked away, and will re-appear
when you switch back to that branch.

Now, switch back to the exp1 branch, and check that the `test.txt` is
now present.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Help-browser.svg/20px-Help-browser.svg.png)
Stuck? Ask for help from the TA

# Merging

We now try out merging. Eventually you will want to merge two branches
together after the conclusion of work.\
`git merge` allows you to do that.

Git merging works by first switching the branch you want to *into*, and
then running the command to merge the other branch in.

We now want to merge our `exp1` branch into `master`. First, switch to
the `master` branch.

    git checkout master

Next, we merge the `exp1` branch into `master` :

    $ git merge exp1

Do you see the following output ?

    Merge made by recursive.
     test.txt |    1 +
     1 files changed, 1 insertions(+), 0 deletions(-)
     create mode 100644 test.txt

You have to be in the branch you want merge *into* and then you always
specify the branch you want to merge.

At this point, you can also try out `gitk` to visualize the changes and
how the two branches have merged

# Merge Conflicts

Git is pretty good at merging automagically, even when the same file is
edited. There are however, some situations where the same line of code
is edited there is no way a computer can figure out how to merge.\
This will trigger a conflict which you will have to fix.

We now practise fixing merge conflicts. Recall that conflicts are caused
by merges which affect the same block of code.

Here’s a branch I prepared earlier. The branch is called `alpher`. Run
the code below to set it up (don’t worry if you can’t understand it)

    $ git checkout alpher

You should now have a new branch called `alpher`. Try merging that
branch into `master` now and fix the ensuing conflict.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Help-browser.svg/20px-Help-browser.svg.png)
Stuck? Ask for help from the TA

# Fixing a conflict

You should see a `conflict` with the `gamow.txt` file. This means that
the same line of text was edited and committed on both the master branch
and the alpher branch. The output below basically tells you the current
situation :

    Auto-merging gamow.txt
    CONFLICT (content): Merge conflict in gamow.txt
    Automatic merge failed; fix conflicts and then commit the result.

If you open the `gamow.txt` file, you will see something similar as
below:

    $ cat gamow.txt
    <<<<<<< HEAD
    It was eventually recognized that most of the heavy elements observed in the present universe are the result of stellar nucleosynthesis (http://en.wikipedia.org/wiki/Stellar_nucleosynthesis) in stars, a theory largely developed by Bethe.
    =======

    http://en.wikipedia.org/wiki/Stellar_nucleosynthesis
    Stellar nucleosynthesis is the collective term for the nuclear reactions taking place in stars to build the nuclei of the elements heavier than hydrogen. Some small quantity of these reactions also occur on the stellar surface under various circumstances. For the creation of elements during the explosion of a star, the term supernova nucleosynthesis is used.
    >>>>>>> alpher

Git uses pretty much standard conflict resolution markers. The top part
of the block, which is everything between `<<<<<< HEAD` and `======` is
what was in your current branch.\
The bottom half is the version that is present from the `alpher` branch.
To resolve the conflict, you either choose one side or merge them as you
see fit.

For example, I might decide to choose the version from the `alpher`
branch.

Now, try to **fix the merge conflict**. Pick the text that you think is
better (Ask for help if stumped)

Once I have done that, I can then mark the conflict as fixed by using
`git add` and `git commit`.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Help-browser.svg/20px-Help-browser.svg.png)
Stuck? Ask for help from the TA

    $ git add gamow.txt
    $ git commit -m "Fixed conflict"

Congratulations. You have fixed the conflict. All is good in the world.

Fin
---

You have learnt :

1.  Clone a repository
2.  Commit files
3.  Check status
4.  Check diff
5.  Undoing changes
6.  Branching and merging
7.  Fixing conflicts



Part II
========

GitHub
------
But, wait. There’s more. What about this distributed sharing thing with
Git ?

To be able to share, we’ll need a server to host our git repositiories.
GitHub (<a href="https://github.com/">github.com</a>) is probably the
easiest place to begin with.

Login or sign up with GitHub
----------------------------

If you've already got an account you can skip on to creating the repo on
github, or forking this repository and cloning it down to your local machine.

Otherwise...

Go <a href="https://github.com/signup">sign up for an account</a> at
GitHub; Or login into your GitHub account if you had previously signed
up.

Hint: You may need to setup git cache your GitHub password - see
<a href="https://help.github.com/articles/set-up-git">https://help.github.com/articles/set-up-git</a>

Then come back here, we’ll wait.

Create your first GitHub repository
-----------------------------------

A repository (repo) is a place where you would store your code. You were
practicing on your very own repo just now in Part 1!

The following <a href="https://help.github.com/articles/create-a-repo">
tutorial</a> will show you how to create a GitHub repo - which you can
then share with others

Then come back here, we’ll wait.

Fork a repo
-----------

Go to [this tutorial](https://help.github.com/articles/fork-a-repo)
Then come back here, we’ll wait.

Let’s collaborate !
-------------------

Check out the `pull_request` branch on this repository for further instructions!
You can always get back to this version of the readme by checking out the master branch.

Finally
---

You have learnt:

1.  Forking a repo at GitHub
2.  Git push
3.  Git pull

### References and Further reading

I thoroughly recommend these resources to continue your Git practice:

-   <a href="http://try.github.com">http://try.github.com</a> Another
    beginners tutorial for git
-   <a href="http://git-scm.com">http://git-scm.com</a> Official
    website, with very useful help, book and videos


<sub><sub><sup>inspired work and credit https://github.com/kuahyeow/git-workshop/tree/master</sup></sub></sub>


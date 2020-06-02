## Git 2: Using and Troubleshooting `git`

### Overview

At first, _Git_ may seem extremely daunting; you will probably think you are going to break something or overwrite some code accidentally. You will be confused about what is happening and where, and you will not be sure why or how things aren't working correctly.

This guide and [the accompanying video][gitWalkthrough] will help to demystify how _Git_ works, give you some simple repetitive steps to follow which will help you stay out of trouble, and help you understand both why things aren't working and how to fix them.

Like most things in software development, understanding _Git_ will come with practice, patience, and by reading the output after running commands.

### 1. `git status`

#### What it does:

Lists file modifications since the last _commit_. In other words, `git status` will list every file that has been changed (lines added/removed, file deleted, file created) since the last time you committed.

#### What it looks like:

![Git Status](images/gitStatus.gif)

* ***What Happened???***

  * `touch newFile.txt` created a new file named 'newFile.txt'

  * `git status` showed me that `newFile.txt` was an untracked file

  * I used `git add newFile.txt` to _stage_ the change to the file.

  * `git status` showed me that `newFile.txt` was _staged_ and ready to be committed.

  * I used `git commit -m "add new file"` to _commit_ the _staged_ changes (the creation of the file).

  * `git status` showed me `nothing to commit, working tree clean` meaning there are no new changes that have been made since the previous _commit_, and I have now _staged_ changes waiting to be _committed_

#### When to use it:
All the time. Whenever you are about to _add_, _commit_, _pull_, or _push_. `git status` is the only way to get information back about the state of your _local repository_, as such, you should use it constantly.

#### Documentation: https://git-scm.com/docs/git-status


<hr>

### 2. `git init`
#### What it does:
Initializes a folder as a _Git Repository_. A _git repository_ tracks changes to files and saves those changes in _commits_ (timestamped save points containing a collection of line changes).

#### What it looks like:
![Git Init](images/gitInit.gif)
* ***What Happened???***

  * I created a new directory with `mkdir newProject` named 'newProject'.

  * I changed directory into 'newProject' with `cd newProject`.

  * I checked where I was in the file system by printing the working directory with `pwd`, which returned '/Users/sdkris/Desktop/newProject', confirming that I was in my new directory.

  * I listed all files in the directory with `ls -a` where the `-a` flag will also show hidden files (file names starting with `.`). This showed that there were no files in the directory.

  * `git init` initialized the directory as a _git repository_ (essentially this creates a hidden directory named `.git`)

  * I confirmed that the directory was a _git repository_ by typing `ls -a` and observing that there was now a hidden `.git` directory (indicating that this directory is a _repository_).

#### When to use it:
When you are starting a new project. Any project that you want to use version control with needs to be created within a _repository_. When starting the project, you should use `git init` to initialize the _repository_.

 * ***NOTE*** you will only need to do this for the top most folder for the project. It is imperative that you not nest _git repositories_ within one another, this will create a _sub module_ (see below), which will lead to problems.

#### Documentation: https://git-scm.com/docs/git-init
<hr>

### 3. `git add`
#### What it does:
Stages changes to files to be committed with the next _commit_.

#### What it looks like:
![Git Add](images/gitAdd.gif)
* ***What Happened???***
  * First I created a new file (example.txt) with `touch example.txt`

  * `git status` shows that example.txt is an untracked file

  * `git add example.txt` stages the change to example.txt (it's creation)

  * `git status` shows that example.txt's creation as a new file is staged and ready to be committed.

#### When to use it:
Whenever you have completed a unit of work and are preparing to _commit_. During pre work, this will probably be every time you write a blog post, or finish an exercise. At a job, this would be whenever you complete a feature, or fix a bug.

#### Documentation: https://git-scm.com/docs/git-add

<hr>

### 4. `git commit -m "some message"`
#### What it does:
Makes a record (save point) of changes in the _repository_.

##### What it looks like:
![Git Commit](images/gitCommit.gif)

* ***What Happened???***
  * After using `git add example.txt` to stage the creation of the file...

  * `git commit -m "create example.txt"` made a new _commit_ (save point) recording that change.

  * The resulting message is:
```bash
[master (root-commit) 69fb6b9] create example.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 example.txt
```
  * This output lets me know what happened,

    * the first line has `create exmple.txt`, that was the message I included with the _commit_ after the `-m` (for message) flag.
    * the second line let's me know that `1 file changed` and how.
    * the third line is letting me know that a new file was created and is being tracked.

  * Alternatively, I could add some contents to the file `example.txt`, stage and commit that :

![Git Commit 2](images/gitCommit2.gif)

  * In this example, I have changed lines in the file (modifying an existing file).

  * When I _commit_ I see:

```bash
[master 22e7849] add content
 1 file changed, 1 insertion(+)
```

  * This output lets me know that `1 file changed` and that `1 insertion(+)`, meaning, one line's content changed and that the change was a line addition.


***NOTE:*** You will not commit _every_ time you change a line or create a file. You should commit when you complete something (e.g. a blog post, or an exercise).

#### When to use it:
After you _stage_ changes with `git add <file>`, and when you have completed something. If you use `git status` and the message is not :

```bash
On branch master
nothing to commit, working tree clean
```

You need to commit to save your work.

#### Documentation: https://git-scm.com/docs/git-commit

<hr>

### 5. `git remote add origin <url>`
#### What it does:
Links a _remote repository_ (located at some url) to the current _local repository_ with the name origin.

#### What it looks like:
![Git Remote Add Origin](images/gitRemoteAddOrigin.gif)

* ***What Happened???***

  * `git remote -v` lists the _remote repositories_ connected to the current _local repository_. At first, when I enter this command, no information prints out, that is because my local is not connect to any remotes.

  * `git remote add origin https://github.com/kkane106/new-repository.git` this command add's a reference to a _remote repository_ at some location (the url) and aliases it by a _shortname_.

  * `git remote -v` now returns :
```bash
origin	https://github.com/kkane106/new-project.git (fetch)
origin	https://github.com/kkane106/new-project.git (push)
```
    * this shows that my _local repository_ is aware of a _remote repository_ named 'origin' located at `https://github.com/kkane106/new-project.git`.

#### When to use it:
When you need to connect a _local repository_ to a _remote repository_. An example would be connecting the project files you are working on on your computer to a Github repository so that you can share them or collaborate on the project with others.

#### Documentation: https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes

<hr>

### 6. `git pull origin master`

#### What it does:
Fetches the commits from the _remote repository_ named 'origin' and attempts to merge them with your _local repository's_ commit history.

_Git_ sees the current state of you application as the sum total of all of the individual line changes that are stored within commits. This allows multiple users to make changes and collaborate simultaneously. Whenever you use `git pull`, you receive the updates that have been made on the _remote repository_ (if there are any) and have them merged into a new _commit_ in your _local repository_ (a commit which saves the changes from the merge).

Commit histories are often represented as a linked list of nodes, like the one below:

![Git log](images/gitLog.png)

This image shows that changes were made to the remote from a single source until the 5th node, sometime after the 5th node, a change was made from another source (blue). During the time that the blue node was being worked on, another commit was made (the 6th black node). Before the blue branch was able to integrate their code back into the main source code (the master branch), it was required to `pull`. Doing so, merged the branches and resulted in a new commit (the 7th black node).

#### What it looks like:
* **Example 1** : No Master
![Git Pull No Master](images/gitPullNoMaster.gif)
* ***What Happened???***

  * After attempting to `git pull origin master`, the message `fatal : Couldn't find remote ref master` appeared.

  * This message means that the remote you tried to pull from does not have any content. ***NOTE:*** this will only happen after initializing a new repository and before you push.

  * ***solution*** : add, commit, and push.

* **Example** 2 : Additional Refs
![Git Pull Additional Refs](images/gitPullAdditionalRefs.gif)
* ***What Happened???***

  * `git pull origin master` merged new commits from the remote (commits you didn't have locally). This automatically updated the files with line changes from those commits.

  * ***NOTE***: this will only happen if the remote changes in isolation of your local (like if you are collaborating with someone, or edit something directly from Github --> which you should not do.)

* **Example** 3 : Merge Conflict
![Git Merge Conflict](images/gitMergeConflict1.gif)
* ***What Happened???***

  * `git pull origin master` merged new commits from the remote and experienced a `CONFLICT`.

  * ***GO TO : 9. Merge Conflicts - Detection and Resolution*** below.

#### When to use it:
***ALWAYS pull before you push***. Anytime you are going to push code, pull first. This is to ensure that you have the most up to date local version (complete with all of the commits from the remote) before attempting to push to the remote.

#### Documentation: https://git-scm.com/docs/git-pull

<hr>

### 7. `git push origin master`
#### What it does:
Sends commits from your _local repository_ to a _remote repository_ aliased as 'origin', and merges the commit histories (updating the remote with you local changes).

#### What it looks like:
* **Example** 1 : First Push
![First Push](images/gitPushFirstPush.gif)
  * ***What Happened???***

    * After attempting to pull.

    * `git push origin master` sent the local commits to the remote.

* **Example** 2 : Subsequent Pushes
![Subsequent Pushes](images/gitPushSubsequentPushes.gif)

  * ***What Happened???***

    * After adding, committing, and attempting to pull.

    * `git push origin master` sent the local commits to the remote.


#### When to use it:
Whenever you have completed a unit of work, after using `git add <file(s)>`, `git commit -m "some message"`, and `git pull origin master`. During pre work this will usually be in service of updating your blog, or sending a completed exercise to Github.

#### Documentation: https://git-scm.com/docs/git-push

<hr>

### 8. `git log`

#### What it does:
Shows the _commit_ history for the current _repository_, can optionally be provided with a numeric flag (`git log -2`) to indicate how many of the previous commits to show.
#### What it looks like:

![Git Log](images/gitLogDetail.gif)

* ***What Happened???***

***TROUBLE***: *Help, I can't get my command prompt back!?!?!?*

* you are probably stuck in read mode (prompted by a `:`). Press the `Q` key to quit this mode:

![Quit Git Log](images/gitLogQuit.gif)

#### When to use it:
When you want to see the difference between two commits, revert back to a previous commit, or view the messages from your previous commits.

#### Documentation:
https://git-scm.com/docs/git-log  
https://git-scm.com/docs/git-diff

<hr>

### 9. Merge Conflicts - Detection and Resolution

#### What it is:
The same line(s) were changed in a file by separate _commits_. Your _local repository_ has one version, and the _remote repository_ has a different version. _Git_ is unwilling to choose which version is correct (it can't decide which version is correct). Instead of arbitrarily choosing one version or the other, it prompts you to decide what to do.

A _Merge Conflict_ is immediately identifiable in the console by the word `CONFLICT` appearing in the output immediately following a `git pull`.

#### What it looks like:
* **Terminal**:

![Merge Conflict Terminal](images/gitMergeConflict1.gif)

  * A line like `CONFLICT (type) : Merge conflict in <file reference>` is a dead giveaway that you have a merge conflict. Go to the file that was referenced, and you will see the line _Git_ got hung up by.

* **Code**:

![Merge Conflict Code](images/gitMergeConflict2.gif)

  * A _Merge Conflict_ will make itself known in code with the following format:

```java
<<<<<<<< HEAD
  /* This is the code from your last commit locally */

========

  /* The code from the remote repository */

>>>>>>>> c7653someUniqueCharacterString
```

#### How to fix it:

![Resolve Merge Conflict](images/gitMergeConflict3.gif)

1. Modify the code in the file as you wish.

2. Remove the following lines :
   * `<<<<<<<< HEAD`
   * `========`
   * `>>>>>>>>> c7564alsjdfnlsajdfnlsjb`

3. `git add <file referenced>`

   * stage the corrected file(s).

4. `git commit -m "some message"`

   * make a new commit with the corrected file(s).

![Resolve Merge Conflict](images/gitMergeConflict4.gif)

_Merge Conflicts_ are scary at first, but they are actually there to help you. _Git_ wants you to modify the code and then recommit the fixed (and successfully merged) version.

#### Documentation: https://git-scm.com/docs/git-merge

<hr>

[Prev](pushToGithub.md) | [Up](README.md)


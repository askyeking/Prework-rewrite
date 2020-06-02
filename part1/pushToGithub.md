## Sharing on Github

### Overview

Now that you have a version-controlled repository and a _commit_, you can share your project with the world (or just fellow collaborators) by sending it to the social / collaborative site _Github_.

For a brief promotional overview of what _Github_ is, check out this commercial they made for themselves: https://www.youtube.com/watch?v=w3jLJU7DT5E

In more technical terms, _Github_ stores central _repositories_ with a bunch of features to visualize changes, track issues, and get some meta information about the project. For our purposes at the moment, we will be using _Github_ as a _remote repository_ which we will push changes to from our _local repository_ (the one we created and made a commit to in the previous step).

How are _Git_ & _Github_ related?

_Git_ is a Version Control Software. _Github_ is a web based collaboration tool which can store it's users _remote (aka central) repositories_

Here is a short video explaining _Git_ workflow and where _Github's_ central repository might fit in: https://www.youtube.com/watch?v=OqmSzXDrJBk

Here is an article explaining the difference between _Git_ and _Github_: https://jahya.net/blog/git-vs-github/

<hr>

### 1. Create a Repository on Github

* Sign into your _Github_ account: https://github.com/login

* Click on the _Repositories_ tab.

![Sign In & Go To Repositories](images/githubSignIn.gif)


* Click the green _New_ button.

* On the "Create a New Repository" page, in the "Repository name" field, enter the name `hello-world`

* Scroll down and click the green, "Create Repository" button.

![Create Repo](images/githubCreateRepo.gif)

<hr>

### 2. Connect the Github Remote Repository to your Local Repository

After creating your _remote "hello-world" repository_, _Github_ navigated you to the _repository's_ dashboard. On this page, there is a link to the _repository_, something like `https://github.com/yourUsername/hello-world.git`. This is the actual location of the _repository_ you just created. Now you are going to connect it to your _local repository_ on your computer.

* Click the "Copy to Clipboard" button next to the _repository's_ address.

* In _Terminal_, navigate to your local `HelloWorld` repository (should be located at `/Users/yourUsername/Desktop/HelloWorld`)

* Link this _local repository_ to the _Github remote repository_ by typing `git remote add origin <your-copied-link-to-your-repository>`

  * ***NOTE***: replace `<your-copied-link-to-your-repository>` with your _remote repository's_ actual address.

* Verify that your _remote repository_ is connected by typing `git remote -v`, this should display the address of your _remote repository_ followed by

![Github Add Remote](images/githubAddRemote.gif)

<hr>

### 3. Send Local Commits to Github's Remote Repository

Now that your _local repository_ knows where it's _remote repository_ is located, we can use _Git_ to communicate between the two.

* Type `git push origin master`.

  * ***Explanation***:
    * ***push***: is the command to send _commits_ to another location
    * ***origin***: is the default alias for the location of our _remote repository_, think of _origin_ as a variable that represents `https://github.com/yourUsername/hello-world.git`.
    * ***master***: the _branch_ (our only _branch_) of _commits_ that we want to send to the _remote repository_

* ***NOTE***: Your first time you may be prompted for your _Github_ username and password. When typing your password, you will not see the characters print out, in fact you won't see anything print out, this is intentional and a security feature. Don't worry, behind the scenes it is registering the keys you type and when you press `return`, it will submit the password you have typed.

* After a brief upload displays it's progress, you should not see any errors and be returned to a command prompt.

* Now you can go to your _Github_ repository page and refresh, you should see the file you pushed.

![Github Push](images/githubPush.gif)

<hr>

[Prev](git.md) | [Up](README.md) | [Next](git2.md)


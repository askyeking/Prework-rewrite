### `cd` & `mkdir` - *Change Directory (navigate through file system), Make Directory (create a folder)*

<hr />

#### Video Guide

<a href="https://youtu.be/SxCufIe3v0o">
  <img src="../images/unix_cd_vid.png" />
</a>

<hr />


* Your terminal window gives you the ability to navigate through and interact with your file system. When you open a new window you placed in your _HOME directory_ by default. On Mac OS, your HOME directory is `/Users/yourAccountName`.

  * In the _bash_ shell the HOME directory is represented by a `~`.

  * The terms _folder_ and _directory_ are interchangeable.

* You can navigate into the file system using a command `cd` or change directory. For example ```cd Desktop``` would move you from your HOME directory to your `Desktop` directory. This is the same as if you were to click on the `Desktop` folder in _Finder_.

* If you want to return to your HOME directory once your are inside your `Desktop` directory, you can traverse back up the file structure with

  ```bash
  cd ..
  ```

  * Or, you can use `~`:

    ```bash
    cd ~
    ```

  * Or, you can just type `cd`, which by default takes you to your HOME.

    ```bash
    cd
    ```

#### `mkdir`- *Make Directory (create a new folder)*

* To make a new folder use the `mkdir` command.

  * In your _Desktop_, create a folder called `notes`

    ```bash
    cd ~/Desktop
    mkdir notes
    ```

* To navigate to this location I would have to go from my HOME to `Desktop` to `notes`.

![cd Command](images/cdCommand.gif)

* If I wanted to go from `Home` to `notes` directly, you can chain the paths into one `cd` command, ```cd Desktop/notes```.

![cd homeToNotes](images/cdHomeToNotes.gif)

* Move the file `introToTheTerminal.txt` into `notes`:

  ```bash
  cd ~/Desktop/notes
  mv ../introToTheTerminal.txt .
  ```

* Lets create a new folder called `unix` inside of our `notes` folder.

  ```bash
  cd ~/Desktop/notes
  mkdir unix
  ```

![mkdir Command](images/mkdirCommand.gif)

<hr>

[Prev](unixCommands.md) | [Up](README.md) | [Next](pwd-ls.md)


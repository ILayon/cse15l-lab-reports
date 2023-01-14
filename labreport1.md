# How to log into ieng6
**By Isabelle Layon**

## Step 1: Installing VS Code
> **Note:** If you have already installed VS Code onto your computer (maybe from a prior CS course!), you can skip to Step 2.

* Before installing VS Code, you will first need to install a Java Development Kit (JDK). Open [this link](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
to install Java 17 for Windows, Mac, or Linux, and complete the setup.
* After the JDK is installed and setup, install VS Code for Windows, Mac, or Linux using [this link](https://code.visualstudio.com/).
* When VS Code, is setup and opened, you will be greeted by this screen:

You will now be able to open/create folders and Java files and access the terminal.

## Step 2: Remotely Connecting
> **Note:** If you are using Windows, you will need to install [Git from this link](https://gitforwindows.org/). This will simplify how paths used in the terminal are displayed such as absolute paths.

> **Bash Terminal**

* First, we will need to learn how to use a Bash terminal. Open a new terminal by clicking on Terminal on the top of the screen, and selecting New Terminal.
* Press CTRL + Shift + P to open the command palette and type **"Select Default Profile"**.
* After clicking on Select Default Profile, click on **"Git Bash"**.
* Now you will be able to select a Bash terminal by clicking on the + button on the terminal menu.

> **Setting up your CSE 15L account**

* Next, make sure you have set up your CSE 15L account. [Lookup your account](https://sdacs.ucsd.edu/~icc/index.php) and set your password (it can be the same as your
regular TritonLink account). Take note of your account's username. It will take around 15 minutes for your password to be activated after setting it.

> **Using the Terminal**

* To get started on remote connecting, type the command `$ ssh **your CSE15L username**`. You will get a message asking if you are sure you want to connect. Type in "yes".
* You will get a prompt to enter in your account password. It will look as if you are not typing anything in while entering it, but the inputs are just invisble.
If you are prompted to enter your password in several times or get an "Access denied" message, check to see if you has mistyped your username or passsword, or wait a few minutes
so that your password is activated.
* After your password has been entered, you will be greeted with a welcome message and a menu similar to this:

## Step 3: Running Commands
* On the remotely connected menu, you are now able to type in commands. For example, using the command `ls /home/linux/ieng6/cs15lwi23/cs15lwi23art` shows the file hello.txt.
Then using the command `cat /home/linux/ieng6/cs15lwi23/public/hello.txt` would print out a welcome message.

> **Congratulations! You have successfully setup VS Code, remote connecting, and have tested commands!**



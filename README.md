# Assignment 0: Command-Line Interface (CLI)

(**Navigation**: Type `q` to exit. Type `b` to go back to the previous page. Type `<Space>` to go to the next page. Type `j` to scroll down by one line. Type `k` to scroll up by one line.)

In this assignment, you will follow an online tutorial on how to use the command-line interface (CLI). CLI has been around for decades and there are many great tutorials online. The particular one that we will use is from [Ryan's Tutorials](https://ryanstutorials.net/), and we think that it is a very nice, introductory-level tutorial for beginners. How long it takes depends on your prior background, but the tutorial is *not* short. Be prepared to spend a few hours on this and start early.

In order to do this, here are the steps that you must follow.

* Use your browser to open the tutorial. The URL is [https://ryanstutorials.net/linuxtutorial/](https://ryanstutorials.net/linuxtutorial/).
* Use a terminal instance as you follow along the tutorial. Try out the commands that the tutorial demonsrates.
* At the end of each section, there are **Activities** that the tutorial asks you to do. You *must* do these activities because *those are what we grade*.
* For grading, you need to record what you do and submit the recording. We use `script`, a program that records what happens in the terminal and saves it to a file. So before you start the tutorial, you need to run `script` and record what you do in a file, and later submit the file when you're done.
* You don't need to do the tutorial in one sitting as `script` allows you to stop recording and resume later.
* More precisely, every time you do the tutorial, follow these steps.
    * Make sure you are in the correct directory for this assignment by entering `cd ~/units/01-intro/a0`.
    * First, enter `script -a`, which starts recording what you do in your terminal and saves it to a file named `typescript`.
    * Follow the tutorial and do the activities. However, there is one exception. For *6. Vi Text Editor* section, whenever the tutorial says enter `vi`, enter `nvim` instead. We do not use the original vi. Instead, we use Neovim, a newer implementation of vi.
    * If you want to stop, enter `exit`, which stops recording.
    * Next time you come back, go to the correct directory (`cd ~/units/01-intro/a0`) and enter `script -a` again. It does not overwrite what you have recorded previously. It just appends to the existing recording.
    * Once you are done with the tutorial and ready to submit, use `git` to push the recording. For that, you can enter the following commands. (Note that `$` indicates the command prompt. Do not enter it.)
    ```bash
    $ cd ~/units/01-intro/a0
    $ git add .
    $ git commit -m "A0 submission"
    $ git push
    ```
    * If you recall, `git add` tells `git` that you want to save the contents of the files or directories that you provide as the arguments (a question here that you should be able to answer from the tutorial that you just did---what is `.`?). `git commit` permanently saves the file contents, and `git push` uploads the saved files to your remote GitHub Classroom repo for the assignment. `git commit` requires a commit message, and in the above, "A0 submission" is the commit message. You are free to replace it with your own message. `git log` shows commit messages.
    * If you'd like to back up what you have been doing at any point, you can enter the above commands even when you are not ready to submit. Again, the commands push your files to your remote GitHub Classroom repo for the assignment.

# Tips

At the end of the tutorial, there is a [cheat sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php) that summarizes basic commands. We highly recommend to open the page in your browser and keep it in the background throughout the semester, so you can easily look up the commands that you want to use.

(**Navigation**: Type `q` to exit. Type `b` to go back to the previous page. Type `<Space>` to go to the next page. Type `j` to scroll down by one line. Type `k` to scroll up by one line.)

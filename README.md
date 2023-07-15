# Assignment 0: Command-Line Interface (CLI)

In this assignment, you will follow an online tutorial on how to use the command-line interface (CLI). CLI has been around for decades and there are many great tutorials online. The particular one that we will use is from [Ryan's Tutorials](https://ryanstutorials.net/), and we think that it is a very nice, introductory-level tutorial for beginners. How long it takes depends on your prior background, but the tutorial is *not* short. Be prepared to spend some serious hours on this and start early.

In order to do this, here are the steps that you must follow.

* Use your browser to open the tutorial. The URL is [https://ryanstutorials.net/linuxtutorial/](https://ryanstutorials.net/linuxtutorial/).
* Use a terminal instance as you follow along the tutorial. Try out the commands that the tutorial demonsrates.
* At the end of each section, there are **Activities** that the tutorial asks you to do. You *must* do these activities because *those are what we grade*.
* For grading, you need to record what you do in your terminal and submit the recording. We use `script`, a program that records what happens in the terminal and saves it to a file. So when you follow the tutorial, you need to run `script` and record what you do in a file, and later submit the file when you're done.
* There is no need to do the tutorial in one sitting as `script` allows you to stop recording and resume later.
* More precisely, every time you do the tutorial, make sure you do the following.
    * Make sure you are in the correct directory for this assignment by entering `cd ~/units/01-intro/a0`.
    * First, enter `script -a`, which starts recording what you do in your terminal and saves it to a file named `typescript`.
    * Follow the tutorial and do the activities.
    * If you want to stop, enter `exit`, which stops recording.
    * Next time you come back, go to the correct directory (`cd ~/units/01-intro/a0`) and enter `script -a` again. It does not overwrite what you have recorded previously. It just appends to the existing recording.
    * Once you are done with the tutorial and ready to submit, enter the following commands. (Note that `$` indicates the command prompt. Do not enter it.)
    ```bash
    $ git add .
    $ git commit -m "A0 submission"
    $ git push
    ```

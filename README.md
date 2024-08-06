# Assignment 0: Command-Line Interface (CLI)

(**Navigation**: Type `q` to exit. Type `b` to go back to the previous page. Type `<Space>` to go to
the next page. Type `j` to scroll down by one line. Type `k` to scroll up by one line. You probably
want to remember these keys now since you need to scroll up and down this document as you read it.)

In this assignment, you will follow an online tutorial on how to use the command-line interface
(CLI). CLI has been around for decades and there are many great tutorials online. The particular one
that we will use is from [Ryan's Tutorials](https://ryanstutorials.net/), and we think that it is a
very nice, introductory-level tutorial for beginners. How long it takes depends on your prior
background, but the tutorial will probably take less than 3 hours.

In order to do this, here are the steps that you must follow.

* Use your browser to open the tutorial. The URL is
  [https://ryanstutorials.net/linuxtutorial/](https://ryanstutorials.net/linuxtutorial/).
* Use a terminal instance as you follow along the tutorial. Try out the commands that the tutorial
  demonstrates.
* At the end of each section, there are **Activities** that the tutorial asks you to complete. You
  *must* complete these activities because *those are what we grade*.
* For grading, you need to record what you do and submit the recording. We have a program named
  `record` that records what happens in the terminal and saves it to some files. So before you start
  the tutorial, you need to run `record`, and later submit the files that it creates when you're
  done. It is important to remember that this records everything that you type in the terminal.
  Thus, do not type in anything sensitive.
* You don't need to do the tutorial in one sitting as you can stop recording and later start
  recording again.
* More precisely, when you work through the tutorial, follow these steps.
    * Make sure you are in the correct directory for this assignment by entering `cd
      ~/units/02-tools/a0-USERNAME` where `USERNAME` is your GitHub username.
    * Always enter `record` first before doing anything else. When `record` is running, the prompt
      will display `[recording]`. Make sure you see it before proceeding.
    * `record` starts recording what you do in your terminal and saves it to the files in a
      directory named `.record`.
    * While recording, make sure that you do not copy and paste anything. If you do, you will get a
      0. If you happen to do it, you will need to remove the entire `.record` directory and start
      the tutorial all over again from the beginning.
    * Work through the tutorial and complete the activities. (There is one thing to note---for *6.
      Vi Text Editor* section, whenever the tutorial says enter `vi`, enter `nvim` instead. We do
      not use the original vi. Instead, we use Neovim, a newer implementation of vi.)
    * If you want to stop, enter `exit`, which stops recording. Note that this does not stop the
      container. It only stops recording. You need to enter `exit` again if you want to stop using
      the container.
    * Next time you come back, make sure you go to the correct directory (`cd
      ~/units/02-tools/a0-USERNAME` where `USERNAME` is your GitHub username) and enter `record`. It
      does not overwrite what you have recorded previously. It just writes to new files for
      recording.
    * Once you are done with the tutorial and ready to submit, you are almost ready to use `git` to
      push your files. However, you need to provide your email and name first. This is a one-time
      setup, and you don't need to repeat this in the future. Below, replace `you@example.com` with
      your SFU email and `Your Name` with your name. You still need the double quotes. `$` indicates
      the command prompt. Do not enter it.

      ```bash
      $ git config --global user.email "you@example.com"
      $ git config --global user.name "Your Name"
      ```

    * Now you can use `git` to push your submission. Below, replace `USERNAME` with your GitHub
      username.

      ```bash
      $ cd ~/units/02-tools/a0-USERNAME
      $ git add .
      $ git commit -m "A0 submission"
      $ git push
      ```

    * ***Your final submission is whatever you `git push` by the deadline.*** When you have your
      final recording, make sure you use `git` to add all the files and push it.
    * If you recall, `git add` tells `git` that you want to save the contents of the files or
      directories that you provide as the arguments (a question here: what is `.` in `git add .`?
      You should be able to answer this question from the tutorial you just finished). `git commit`
      actually saves the file contents, and `git push` uploads the saved files to your remote GitHub
      Classroom repo for the assignment. `git commit` requires a commit message, and in the above,
      "A0 submission" is the commit message. You are free to replace it with your own message. `git
      log` shows commit messages.
    * Normally, you should avoid using `git add .` since it's going to blindly `git add` all the
      files. Instead, you should pick and choose the correct files that you want to add and list
      them separately, e.g., `git add <file0> <file1> ...`. The only reason we're doing `git add .`
      in this assignment is that for some students, this is the first time using `git` and the
      command-line interface and we want to simplify the submission for them.
    * If you'd like to back up what you have been doing at any point, you can enter the above
      commands even when you are not ready to submit. Again, the above commands push your files to
      your remote GitHub Classroom repo for the assignment.

## Important Note

You ***should not*** copy and paste the code or command examples. You have to type them yourself
and understand the meanings. If you copy and paste, you ***will not*** get any credit for this
assignment.

# Git Workflow

We have explained this previously, but we want to emphasize this once again.

* `git clone <URL>`: This command clones (i.e., copies) a remote code repo at the URL to your local
  machine. This is typically the very first thing you do.
* `git add <file0> <file1> ...`: This command tells `git` that you want to save the contents of
  `file0`, `file1`, ....
* `git commit -m <message>`: This command permanently saves the contents of the added files from
  previous `git add` commands. You need to provide a short message that describes what this commit
  is for. You can view these messages with `git log` command.
* `git push`: This command pushes (i.e., uploads) all the committed files to the remote repo i.e.,
  the repo that you cloned from using `git clone`.

Git is a very powerful tool for version control and collaboration, and it is part of every
developer's workflow these days. Although we do not really teach Git other than telling you to use
the above commands, we highly encourage you to learn it by yourself. You can start by taking a look
at GitHub's [Quickstart](https://docs.github.com/en/get-started/quickstart) page.

# Tips

At the end of the tutorial, there is a [cheat
sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php) that summarizes basic commands. We
highly recommend you to open the page in your browser and keep it in the background throughout the
semester, so you can easily look up the commands that you want to use.

# Other Features

The shell you use on this VM is called [zsh](https://www.zsh.org/), which is different from
[bash](https://www.gnu.org/software/bash/) that the tutorial uses. We use zsh because it is easier
to customize and has some convenient features that bash does not have. For example, we have
customized zsh on this VM as follows.

* You might have noticed that as you type in a command, it shows a suggestion. Pressing the right
  arrow accepts the suggestion.
* Pressing `<Ctrl>-r` opens your command history with a tool called
  [fzf](https://github.com/junegunn/fzf). fzf is a *fuzzy* finder that matches partial strings. This
  allows you to easily find a command that you have typed in before.
* Pressing `<Ctrl>-t` opens fzf to find files located below the current directory in the file
  hierarchy. You can use this to quickly find a file.
* You might have noticed that the right most side of the command line shows git information such as
  the current git [*branch*](https://shorturl.at/dmt24) and the modification status.
* This is not specific to zsh, but instead of `ls`, you can use
  [`exa`](https://github.com/ogham/exa), a more modern implementation of `ls` that has some useful
  features.

# Next Steps

You need to accept the invite for the next assignment (A1). The process is the same as the last time.

* Get the URL for A1. Go to the URL on your browser.
* Accept the invite for Assignment 1 (A1). It creates a private repo for you that contains the
  assignment.
* After your repo is created, click the URL displayed on the page to go to your repo.
* If you are not in `units/02-tools` directory, go to that directory by entering `cd
  ~/units/02-tools`.
* Enter `git clone git@github.com:SFU-CMPT-201/a1-USERNAME.git` but replace USERNAME with your
  actual GitHub username.
* This clones the assignment under a new directory named `a1-USERNAME` (where USERNAME is still your
  GitHub username) under `units/02-tools` directory.

# Note

From now on, we will not show the navigation instructions for `glow`. Keep using `glow -p` to read
the Markdown files (`.md`) but remember the navigation keys.

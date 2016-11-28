# git-prompt

Git Prompt: a function for adding nominal git info to the Linux Bash command prompt.

**Currently includes**

1. Indicators of:

  * untracked, modified, or added files to the index.
  * merge conflicts.
  * sync with origin(+ is ahead, - is behind)
  * incomplete/complete merge/rebase
  
2. The current branch and refname for HEAD

**Usage**

Copy/paste the code in the file at the end of your .bashrc file. The extra info shows for all git repositories.
Commands: As it is now, this utility is not designed to take any input from the user. I could get around to adding a settings file sometime, but that's about it.

**Acknowledgements**

Contains code taken from http://www.opinionatedprogrammer.com/2011/01/colorful-bash-prompt-reflecting-git-status/

Thanks to Jo Liss for letting me use her code in my project. It's much appreciated.


If you have any suggestions, feel free to post them. Pull requests also welcome.

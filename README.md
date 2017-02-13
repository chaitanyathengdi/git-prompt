# git-prompt

Git Prompt: a function for adding nominal git info to the Linux Bash command prompt.

**Currently includes**

1. Indicators of:

  * untracked, modified, or added files to the index
  * merge conflicts
  * sync with origin(+ is ahead, - is behind)
  * incomplete/complete merge/rebase
  * stashed changes
  
2. The current branch and refname for HEAD

**Usage**

Copy/paste the code in the file at the end of your .bashrc file. The extra info shows for all git repositories. Shows only in the working directory - not in a bare repository or inside the <i>.git</i> folder.

Commands: As it is now, this utility is not designed to take any input from the user. I could get around to adding a settings file sometime, but that's about it.

**Indicator glossary**

<table>
	<tr><th>Indicator</th><th>Color</th><th>Meaning</th></tr>
	<tr><td>S</td><td>Blue</td><td>You have stashed changes.</td></tr>
	<tr><td>C</td><td>Red</td><td>The latest action(cherry-pick, merge, rebase, ...) caused conflicts.</td></tr>
	<tr><td>U</td><td>Red</td><td>Untracked files are present in your directory.</td></tr>
	<tr><td>M</td><td>Red</td><td>You have modified files that are not added to index.</td></tr>
	<tr><td>A</td><td>Green</td><td>Files are present in index.</td></tr>
	<tr><td>Mrg</td><td>Red</td><td>Unfinished merge(due to conflicts).</td></tr>
	<tr><td>&nbsp;</td><td>Green</td><td>Finished merge - make commit to proceed.</td></tr>
	<tr><td>Rbs</td><td>Red</td><td>Unfinished rebase - the current commit has conflicts.</td></tr>
	<tr><td>Cont</td><td>Green</td><td>Conflicts fixed - proceed(with creating commit or continuing rebase/cherry-pick).</td></tr>
	<tr><td>HEAD detached at</td><td>Red</td><td>Similar to 'git status', indicates a detached HEAD state.</td></tr>
	<tr><td>+m/0</td><td>Green</td><td>You are <i>m</i> commits ahead of origin - push your changes.</td></tr>
	<tr><td>0/-n</td><td>Blue</td><td>(After you do a fetch) you are behind origin by <i>n</i> commits. Merge changes.</td></tr>
	<tr><td>+m/-n</td><td>Green/Blue</td><td>Both of the above at the same time(indicates a diverged branch - do a rebase)</td></tr>
</table>

**Acknowledgements**

Contains code taken from http://www.opinionatedprogrammer.com/2011/01/colorful-bash-prompt-reflecting-git-status/

Thanks to Jo Liss for letting me use her code in my project. It's much appreciated.


If you have any suggestions, feel free to post them. Pull requests also welcome.

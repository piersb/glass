# Uninstalling
First off, if you're uninstalling because of some unexpected behaviour. feel free to create [an issue](https://github.com/timeglass/glass/issues) that explains your problems. I love being in conversation with the user to create the best experience possible. 

That being said, you can do the following in order to remove Timeglass from a single repository:

1. Stop the timer by running `glass stop`. If it's not running thats OK, you can skip this step.
2. Remove the git hooks timeglass creates from the `.git/hooks` directory of your repo. The following files are created during installation:

     - .git/hooks/prepare-commit-msg
     - .git/hooks/post-commit 
     - .git/hooks/pre-push

If you would like to continue and remove Timeglass from your system entirely, do the following:

1. Uninstall the background process by running `sudo glass uninstall`. If its not running thats OK, you can skip this step. Windows requires you to run this command as the administrator.
2. Remove the system-wide data directory: `/Library/Timeglass` on OSX, `/var/lib/timeglass` on Linux and `%PROGRAMDATA%\Timeglass` or `%ALLUSERSPROFILE%\Timeglass` on Windows.
3. Remove the binaries itself from were you installed them, they're named `glass` and `glass-daemon`.

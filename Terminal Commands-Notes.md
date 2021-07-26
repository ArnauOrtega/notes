# General Notes

* To copy text from the terminal, use `CTRL + SHIFT + C`. Likewise, to paste into the terminal, use `CTRL + SHIFT + V`.
* Anatomy of a command: `command -flags --flags args`
* For programs that don't have a `man` page, you can try the following: `program -h` or `program --help`
* A single hyphen (`-`) can be followed by multiple **single-character** flags, while a double hyphen (`--`) prefixes a single **multicharacter** option.
* Piping (`|`) connects the input and output of two commands. When piping, the output of the 1st program is sent to the input of the 2nd program.
* To start a program in the _background_, end it with an `&`, in the command line.
* If you ever see a `>` in the terminal it's because the shell is now waiting on input.
* Use a `*` at the end of an incomplete filename to indicate that you're only interested in looking for filenames that begin with what came before the `*`. This works vice versa too.
* `my\ new\ file.txt` or `"my new file.txt"` is an example of how to use literal spaces.
* Operators used to combine commands:
	* `A ; B ` -- Run A and then B, regardless if A succeeds or fails
	* `A && B`  -- Run B only if A succeeds
	* `A || B`  -- Run B only if A fails
  
* `sh` vs `./`: 
	* Running `sh script` makes dash interpret that script
	* `./ script` tries to find out which interpreter to use by looking at the first line (the bang line, e.g. `#!/bin/bash`), as opposed to running that script.

* Difference between **sourcing** and **executing** a script:
	* Sourcing a script will run the commands in the _current_ shell process, and changes to the environment take effect only in the current shell.
	* Executing a script will run the commands in a _new_ shell, and when the script is done the new shell is terminated
	* **Rule of thumb**: Use source if you want the script to change the environment in your currently running shell, use execute otherwise.

# Directories

| Directory | Where it leads to |
| --- | --- |
| `~` | Home directory |
| `/` | Root directory |
| `.` | Current directory |
| `..` | Parent directory |
| `-` | Previous directory (only for cd) |


# Core Commands

| Command | Result |
| --- | --- |
| `man` | Open the manual/help page for a given command | 
| `cd` | Change directory |
| `ls` | List directories |
| `pwd` | Print working Directory |
| `rm` | Remove file |
| `rmdir` | Remove directory |
| `mkdir` | Make directory |
| `mv` | Move directory. Can be used to rename files too (set the source as the destination) |









# Other Good to Know Commands/Subcommands

| Command | Result |
| --- | --- |

| `rm -r` | Remove a directory and all files that are in it. Also recursively deletes nested directories |
| `rm -I` or `rm -i` | To confirm each file removal |
| `rm -v` | State that the file was removed |
| `rm -f ` | To avoid being asked about removing files, add the -f ("force") option. |
| `grep` | Search for text in files |
| `find` | Search for filenames, inside the directory you're currently at |
| `file name` | Tells you the file type of _name_ |
| `which <...>` | Used to find the location of executable functions |
| `echo` | Display text/string that is passed as an argument |
| `echo "Hello!" >> myfile.txt` | Append text to the end of the file. Note that `>>` means adding a new line to the file while `>` simply overwrites everything.|
| `echo $(( stuff ))` | To do math with integers |
| `echo $SHELL` | Tells you what your home directory is |
| `history` | Print your command line history |

| `ls -l` | Print a list of directories, but with more of their metadata |
| `ls -lh` | Same as above, but more human-readable | mkdir -p _parent/child_ | Create a “chain” of directories |
| `ls -F` | Tell the difference between files and directories |
| `ls -a`| Show all files, including dot files |
| `ls -t` | New files appear first |
| `ln -s <full file directory> <new directory>shortcut_name` | Create a relative link. The file directory should be written out in full (ie. including /home/user/…). Note, the directory of a shortcut is often placed in the "bin" folder, so you can type "shortcut_name" anywhere in the terminal to access it |
| `readlink -m <shortcut name>` | Prints the directory of where that shortcut name is |
| `cp `<target file/directory>` `<destination directory>` | Copy _target file/directory_ to _destination directory_ |
| `cp -r <...> <...>` | Copy directories along with their contents |
| `diff --report-identical-files <...> <...>` | Compares two files to see if they match in content |
| `head` | Print the first 10 lines of a file. You can also add _-n #_, where # is the amount of lines you'd like to show |
| `tail` | Print the last 10 lines of a file. You can add -n # too
| `touch file.txt` | Creates a file with that name. Also updates the aces data/ modification date. |
| `less` | Eextends the capabilities of more. The latter was created to view the content of a file one screenful at a time. less adds features such as backward movements and better memory management. Usually used for longer files |
| `cat` | Concatenates files and prints the result on the standard output. Usually used for short files |
| `mkdir -p parent/child` | Create a “chain” of directories |
| `rmdir` | Remove a directory |
| `kill`/`killall` | Terminate a process |
| `mount`/`umount` | Mount/ unmount devices |
| `jobs` | Lists all jobs |
| `bg #` | Places the current (if there's one) or specified job in the background, where # is the job ID
| `fg #` | Brings the current (if there's one) or s |ecified job into the foreground, where n is the job ID |


| `clear` | Clear the screen |


# Rarer But Powerful Commands
| Command | Description |
| --- | --- |
| `wget url` | Used to download files from the internet |
| `tee file` | Output to terminal and save to file |
| `nmcli` | Network/wifi/ethernet information |
| `HISTTIMEFORMAT="%F %T "`| Set the Bash history to show a timestamp for your command history (for the current terminal session only). Now type history and you should see timestamp for your Bash history. |
| `export` | Export is a built-in command of the Bash shell. It is used to mark variables and functions to be passed to child processes. Examples include $HOME and $PATH. |
| `wc` | Print info about a file |
| `df` | Display disk space usage |
| `chmod +x file`| To make files executable |
| `lsusb` | Display which USB ports are being used and by what |

# Brace Expansion (Rare Too)

* Below brace exanpsion will be described via the following set of examples
* Take careful notice on the spacing, it's important

| Example | Result and/or Comments |
| --- | --- |
| `echo "I love "{Bach,Beethoven,Brahms}` | "I love Bach I love Beethoven I love Brahms" |
| `echo {a..z}` | "a b c d e f g h i j k l m n o p q r s t u v w x y z" |
| `echo {1..9}` | "1 2 3 4 5 6 7 8 9" |
| `mkdir {2008..2017}-{01-12}` |  Makes directories for all 12 months in all those years |

# Related To Sudo
| Command | Description |
| --- | --- |
| `sudo apt list --installed` | To show list of all apt installed packages |

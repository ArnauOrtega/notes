# Vim Commands

Below are the most useful Vim Commands I have found.

# At The Terminal

| Command | Description |
| --- | --- |
| `-M` or `-R` | File modifications are not allowed |
| `-x` | Activate encryption when writing files |
| `--version` | Print your Vim version |

# In The File

**Note:**
* A "word" starts/ends at a non-word character, such as a ".", "-", or ")".
* A "WORD" ends strictly with a white-space.
* For most commands below, you can attach a number (#) at the start of it to repeat that command that # of times.

# Cursor Movement

| Keystrokes | Action |
| --- | --- |
| `h/j/k/l` | Move cursor left/down/up/right, respectively |
| `CTRL + d` | Scroll down one half of a screen |
| `CTRL + u` | Scroll up one half of a screen |
| `CTRL + f` | Scroll forward one screen |
| `CTRL + b` | Scroll back one screen |
| `W`  | Move cursor to the start of the next WORD | 
| `w` | Move cursor to the start of the next word |
| `B` | Move cursor to the start of the previous WORD | 
| `b` | Move cursor to the start of the previous word |
| `E` | Move cursor to the end of the next WORD | 
| `e` | Move cursor to the end of the next word |
| `0` | Move cursor to the beginning of the line |
| `$` | Move cursor to the end of the line |
| `:#` | Move cursot to line number # |
| `G` | Move cursor to the end of the file |
| `gg` | Move cursor to the beginning of the file |
| `%` | Move cursor to the matching bracket; (){}[] |
| `m*` | Mark the line on which the cursor resides by the letter * |
| `'*` | Move cursor to the line marked m* |

# Editing

## Inserting

| Keystrokes | Action |
| --- | --- |
| `i` | Insert at cursor |
| `I` | Insert at the character before the cursor |
| `a` | Append after the cursor |
| `A` | Append at the end of the line you're at |
| `o` | Open a new line below the current line you're at |
| `O` | Open a line above the current line you're at |
| `C` | Delete the contents of line after the cursor and enter insert mode |

## Deleting
| Keystrokes | Action |
| --- | --- |
| `D` | Delete contents of line after cursor |
| `x` | Delete character at cursor |
| `X` | Delete character before cursor |
| `dd` | Delete the current line |

## Yanking and Putting

**Note:**
* Deleting _yanks_ that content for you too

| Keystrokes | Action |
|---| ---|
| `yy` | Yank a line | 
| `p` | Put what was last yanked, after cursor position |
| `P` | Put what was last yanked, before cursor position |

## Misc./Other Edits

| Keystrokes | Action |
|---| --- |
| `v` | Enter visual mode, where you can select text by moving around with h/j/k/l or other cursor movement commands |
| `V` | Visually select the line you're at |
| `u` | Undo last change |
| `U` | Undo all changes to entire line |
| `CTRL + r` | Redo the last undo you did |
| `CTRL + a` | Increment the number under your cursor | 
| `CTRL + x` | Decrement the number under your cursor |
| `>>` or `<<` | Shift block to the right or left, respectively |

# Replacing 

| Keystrokes | Action |
|---| ---|
| `r` | Replace 1 character |
| `R` | Replace characters from cursor and on onward |
| `s` | Substitute 1 character and continue in insert mode|
| `S` | Substitute entire line and begin to insert at beginning of line |
| `J` | Join current and next line into one line |

# Searching

| Keystrokes | Action |
| --- | --- |
| `/string` | Search forwards for _string_ | 
| `?string` | Search backwards for _string_ |
| `/\<string/>` | Strictly searching for _string_. This means ignore words that contain "string" as part of a bigger word (ie. the mother in motherboard) |
| `n` | Find the next occurance |
| `N` | Find the previous occurance |

# In Vim's Command Mode

## Files
| Keystrokes | Action |
| --- | --- |
| `:wq` | Save changes to current file and quit |
| `ZZ` | Save changes to current file and quit |
| `:w` | Save changes to current file |
| `:w filename` | Save changes to a new file |
| `:f` | List file information |
| `:q!` | Ignore changes and quit |
| `:x` | Activate encryption |

## Set

| Keystrokes | Action |
| --- | --- |
| `:set ic` and `:set noic` | Case sensitive searches |
| `:set nu` and `:set nonu` | Display line numbers |
| `:set key=` | An empty key option will disable encryption|
| `:set list` | show whitespace (kinda)

## Find and Replace

| Keystrokes | Action |
| --- | --- |
| `%s/aaa/bbb/` |  For all lines in a file, find string 'aaa' an replace with string 'bbb', for the first instance on a line |
| `:%s/aaa/bbb/g` | For all lines in a file, find string 'aaa' an replace with string 'bbb', for all instances on a line |
| `:%s/aaa/bbb/gc` | For all lines in a file, find string 'aaa' an replace with string 'bbb', for all instances on a line. Ask for confirmation |
| `:%s/aaa/bbb/gi` | For all lines in a file, find string 'aaa' an replace with string 'bbb', for all instances on a line. Case insensitive |
| `: #,## stuff` | Between line # and line ##, do _stuff_, which are the commands listed above |

## Misc./Other Commands

| Keystrokes | Action |
| --- | --- |
| `:! command` | Run any _command_ inside Vim (Recall, your current directory is with respect to that of your current file) |



#CLI(Command Line Interface)2

**Standard Output**
- Standard output is screen
- ">": Redirect output after a command(e.g., ls) to create and save the output in a file
```sh
$ ls -lh > file_list.txt
```
- "Cat(command)": displays the content of a text file
```sh
$ cat file_list.txt
```
-">>": Appends output to an existing file, or create and write to a new file doesn't exist
```sh
$ ls -lh >> file_list.txt
```

**Standard Input**
- Standard input is from keyboard
- "<": redirect input from a file
```sh
$ sort < word.txt > sorted_words.txt
```
---

**"|(pipeline)"**
- Pipeline feeds output of previous command to input of next command

**Espansion**
- Special characters expand its meaning when given to shell commands

**Backslash**
- Backslash can be used to ignore line change in command, to enter a long command in multiple lines

**Permissions**
- Files and directories have a permission assigned differently to owner / group / others
```sh
$ -rw-r--r-- 1 owner user
```
 -> owner can read&write user can read only

**Changing Permission**
- "chmod": change permission
```sh
$ chmod 600 README.md
```
 -> 6 = 110 = rw- for owner(owner can r&w but no e)
    
 -> 0 = 000 = --- for group(no r&w&e)
   
 -> 0 = 000 = --- for others(no r&w&e)

|Value|Meaning|
|---|---|
|777|(rwxrwxrwx) No restriction on permissions. Anybody may do nothing. Generally not a desirable setting.|
|755|(rwxr-xr-x) The file's owner may read, write, and excute the file. This setting is common for programs that are used by all user.|
|700|(rwx------) Only the file's owner may read, write, and excute the file. This setting is useful for programs that only the owner may use and must be kept private from others.|
|666|(rw-rw-rw-) All users may read and write the file.|
|644|(rw-r--r--) The owner may read and write a file, while all others may only read the file. A common setting for data files that everybody may read, but only the owner may change.|
|600|(rw-------) The owner may read and write a file. All others have no rights. A common setting for data files that the owner wants to keep private.|

**Superuser**
- Has all system administation authority
- Some commands need superuser's privilleges
- Put "sudo" before the command if you are a superuser

**Text Editors**
|Name|Description|Interface|
|---|---|---|
|vi, vim|On the bright siede, ***vi*** is powerful, lightweight, and fast. Learning ***vi*** is a Unix rite of passage, since it is universally available on Unix-like system. ***vim*** is a remarkable editor and well worth taking the time to learn it.(vim is enhance version of ***vi***)|command line|
|Emacs|Emacs contains every feature ever conceived of for a text editor.|command line|
|nano|***nano*** is a free clone of the text editor supplied with the ***pine*** email program. ***nano*** is very short on features compared to ***vi*** and ***emacs***.|command line|
|gedit|***gedit*** is the editor supplied with the GNOME desktop environment. ***gedit*** is easy to use and contains enough features to be a good beginner-lv editor.|graphical|
|Kwrite|***Kwrite*** is the "advanced editor" supplied with KDE. It has syntax highlighting, a helpful feature for programmers and script writers.|graphical|

-> Tip: History
- Type “history” to see previous command history.
- Or, save it to a text file.

**Wget**
- wget: Download files from the internet directly to your active directory

**Grep**
+ Common Options
  + **i** : Case-insensitive search
  + **v** : Invert the match
  + **n** : Display line numbers along with matching lines.
  + **r** : Recursive search
+ grep supports powerful regular expressions for more complex searches.
  + .* : Matches any character ( . ) zero or more times ( * ).
  + **\d** : Matches any digit (0-9).
  + **[abc]** : Matches any single character within the brackets.
  + **^** : Matches the beginning of a line.
```sh
$ : Matches the end of a line.
```


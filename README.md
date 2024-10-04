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
|777|(rwxrwxrwx) No restriction on permissions. Anybody may do nothing. Generally not a desirable setting|
|755|, this setting is common for programs that are used by user|
|700|(rwx------) Only the file's owner may read, write, and excute the file|
|700||
|700||
|700||

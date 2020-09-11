# Commands for bash

#### cd
- **cd** /folder : Move between folders.
- **cd** .. /directory : Take back 1 level and change to a directory in one move. 

#### mkdir
- **mkdir** directory_name : Creates a directory.

#### rmdir
- **rmdir** : Delete a directory.

#### history
- **history** : Show the history of your commands.

#### clear
- **clear** : Clear the screen.

#### nano
- **nano** name.extension: Creates a file with a specified direction. To create a hidden file the name has to start with '.'

#### cat
- **cat** file : Shows on screen the content of a file.

#### man
- **man** command : Display a screen that shows the information of a command and its options. Example: man ls

#### rm
- **rm** file*.txt : Deletes all the files that start with the specified name, then something else and end with the specified extension.
- **rm -R** /directory : Delete a directory in a recursive way 

#### mv
- **mv** file newname : Change the name of a file 
- **mv** file /destination : Move a file between directories 

#### groups
- **groups** : Show the groups.

#### cp
- **cp** file1 file2 : Copy the first file to another file
- cp -i *.txt : Copy in the previous directory all the txt files 
- **cp -R** dir1 dir2 : Copy the directory 1 to the directory 2. It is important to use -R wich means Recursive. 
- **cp -R** /direction/ destination: Copy the absolute direction where we are.
- **cp -R** -/direction/ ./destination: Copy the current directory
- **cp** * ../directory/. : Copy the files from a specified directory in the current direction

#### help
- **help** command: Show on screen the information of commands and related commands.

#### alias
- **alias** command='other_command': Set an alias to use and summarize a comand for one shorter.

#### whatis
- **whatis** command : Display a header of the manual.

## For Search
#### ls
- **ls** .* : Show the hidden files 
- **ls** -l : Show the files in a list format showing the permissions of user, group, global.
- **ls -a** : Show all the content, including the hidden content. It shows a point and two points at the beginning.
- **ls -A** : Show all the content, including the hidden content.
- **ls -Al** : Show everything (permissionsin, hidden files, bytes) in a list format.
- **ls -Alh** : Show everything (permissionsin, hidden files, bytes) in a list format. It only change in the representation of human language.
- **ls name** : Look for directories/files with that start with an specific name
- **ls** name?name* : Gives the content from the directory. The ? sign means 1 character.
- **ls name*name** : Gives the content from the directory. The * sign means 0 or more characters.
- ls name\*name\* : Gives the content from all the directories. The * sign means 0 or more characters.
- **ls name[[:digit:]]name** : Look for the files in the directories that start with an specific name, then a digit, and end with and specific name.
- **ls name[[:alpha:]]name** : Look for the files in the directories that start with an specific name, then a alphabetic character, and end with and specific name.
- **ls name[[:alnum:]]name** : Look for the files in the directories that start with an specific name, then a alphanumeric character, and end with and specific name.
- **ls name[[:lower:]]name** : Look for the files in the directories that start with an specific name, then a alphabetic lower character, and end with and specific name.
- **ls name[[:upper:]]name** : Look for the files in the directories that start with an specific name, then a alphabetic upper character, and end with and specific name.

#### locate
- **locate** word : Search in the whole computer the specified word. Example: locate teams
- **locate [[:lower:]]** word : Search in the whole computer a word that starts with an alphabetic lower character, and end with and specified name.

#### find
- **find** . -name "file name" : Return all the routes where the file mentioned appears.
- **find / -name filename** : The bar means that finds in the source folder.
- **find . -atime +100** : Files that are in a folder, that where open 100 days ago.
- find / -name *.txt -fprint new_file_to_print.txt : Print all the .txt files in a specified new file.

#### type
- **type** ./file: Tells the origin of an order and the type of file. Example: type cut.

#### stat
- **stat** file_name : Show the statistics of a file, size, block, access (permissions), modifications, changes.

#### chmod
- **chmod +x file_name** : Give execution permissions to the user, group, global.
- **chmod 0### file_name** : Change the permissions for a specific file. Example: chmod 0777 my_file.txt
    - List of the permissions:
    
| rwx | number |
|-----|--------|
| --- | 0      |
| --x | 1      |
| -w- | 2      |
| -wx | 3      |
| r-- | 4      |
| r-x | 5      |
| rw- | 6      |
| rwx | 7      |

### 5 examples of find
- find / -name "my_file_[[:digit:]]_luis*"
- find . -name "new_document_[[:alnum:]].txt*"
- find . -name "document_[[:digit:]]_test_[[:upper:]].*"
- find . -name hello_world_[[:digit:]]_[[:alpha:]]_[[:upper:]].*
- find / -name "[[:alpha:]]_new_document_[[:digit:]].*"

## Manipulation

#### head
- **head** file : Shows the first 10 lines of the file.
- **head -n** # file : Show the first n lines of the file you want. Example: head -n 20 file.

#### tail
- **tail** file : Shows the last 10 lines of the file.
- **tail -n** # file : Show the last n lines of the file you want. Example: tail -n 20 file.

#### wc
- **wc** file : Shows the number of lines, words, characters in the file.
- **wc** \*.extension : Show the number of lines, words, characters in all the files with the specified extension.
- **wc -l** file : Show the number of lines of a file
- **wc -m** file : Show the number of characters of a file
- **wc -lm** file : Show the number of characters and lines of a file

#### sort
- **sort** file : Sort the lines alphabetically.
- **sort -n** file : Sort the lines numeric ascending.
- **soft -n -r** file : Sort the lines numeric descending.

#### column
- **column** -s"separator" -t file :  From a file replaces the specified separator and replaces for another one. Other example: column -s"\t" -t file

#### shuf
- **shuf -n** # file: Take n random lines from a file. Example: shuf -n 5 file

#### grep
- **grep "word"** file : Find the lines where the specified word is located.
- **grep -v "text"** file : Show the lines that doesn't have the pattern

#### touch
- **touch** file: Creates an empty file or convert an existing file in empty

#### cut
- **cut -d"delimitation" -f#** file : Cut the defined element in the assigned delimitation (character) from a file. Example: cut -d"," -f3 my_file.csv
- **cut -d"delimitation" -f# #** : Cut the defined element in the range for the assigned delimitation (character) from a file. Example: cut -d"," -f1 5 my_file.csv

#### unic
- **unic -c** file : Counts how many times all the words appear in a specified file.

#### echo
- **echo "word" > new_file** : Creates a line with the word in the file. If you do it again, it replaces the last line.

## File Download & Processes

#### wget
- **wget** url : Download information from different protocols on internet. It supports HTTP, HTTPS, FTP.
- **wget -i** file : Dowload the information from a file with the link inside of it.
- **wget -O name.extension** url : Saving the information from the link in creating a specified file.
- **wget url &** : While the download is running we can use different commands.
- **wget -i file(with link) 2> /dev/null** : Avoids to show on screen the download processes, it only shows if its an error.
- **wget -i -limit-rate=#kb url** : Avoids to use all the bandwidth in a download, and you can specify how much you want. Example: wget -i -limit-rate=#5kb url

#### curl
- **curl** url : Read the file and show it on screen.
- **curl -o** file url : Download and save the information of the document from the url in the specified file.
- **curl --limit-rate #kb url** : Avoids to use all the bandwidth in a download, and you can specify how much you want.

#### gedit
- **gedit** file : Open the file in another window for editing, but we can not execute commands in the terminal while using.
- **gedit** file **&** : Open the file in another window for editing at the background. We can run commands in the terminal while using it.

#### bg
- **bg** : Reactivates the last process at the background.

#### top
- **top** : Show the processes that are executing.

### Variables
- **variable="Text in a variable"** : Creates a variable
- **echo ${variable} >>** file : Adds the variable to the file

## Pipes
Pipe are redirectioners and we use it with **|**
#### Examples and Applications:
- **echo "Hello World" | wc** : Hello world if the entry and the output is going to be the number of lines, words and characters from the string.
- **sort -nr file | grep "word"** : Find and show the lines where the specified word is in the sorted file in the numeric and reversed way.
- **tail -n 14 file | head -n 1** : Show the first line from a previous tail of 14 elements taken in a file.
- **head -n 10 file | tail -n 1 | wc** : Count the number of lines, words and characters for the last line from the 10 first lines of a file.
- **stat file | grep "word" | cut -d" " -f2** : From the statistics of a file, take the line of a specific word, then cut the information in the 2 of the delimiter " ".

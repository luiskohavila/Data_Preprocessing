## Commands for bash
- **cd** folder/ : Move between folders
- **mkdir** folder_name : 
- **history** : Show the history of your commands
- **clear** : Clear the screen
- **nano** name.extension: Creates a file with a specified direction. To create a hidden file the name has to start with '.'
- **cat** file : Shows on screen the content of a file
- **cp** file1 file2 : Copy the first file to another file
- cp -i *.txt : Copy in the previous directory all the txt files 
- **cp -R dir1 dir2** : Copy the directory 1 to the directory 2. It is important to use -R wich means Recursive. 
- **cp -R** /direction/ destination: Copy the absolute direction where we are.
- **cp -R** -/direction/ ./destination: Copy the current folder
- **man** command : Display a screen that shows the information of a compant and its options. 
- **rm** file*.txt : Deletes all the files that start with the specified name, then something else and end with the specified extension.
- **rmdir** : Delete a directory
- **ls** .* : Show the hidden files 
- **rm -R** /directory : Delete a directory in a recursive way 
- **cd** .. /directory : Take back 1 level and change to a directory in one move. 
- **mv** file newname : Change the name of a file 
- **cp** * ../directory/. : Copy the files from a specified directory in the current direction
- **mv** file /destination : Move a file between folders 
- **ls** -l : Show the files in a list format showing the permissions of user, group, global.
- **ls -a** : Show all the content, including the hidden content. It shows a point and two points at the beginning.
- **ls -A** : Show all the content, including the hidden content.
- **ls -Al** : Show everything (permissionsin, hidden files, bytes) in a list format.
- **ls -Alh** : Show everything (permissionsin, hidden files, bytes) in a list format. It only change in the representation of human language.
- **groups** : Show the groups.

### For Search
- **ls name** : Look for directories/files with that start with an specific name
- **ls** name?name* : Gives the content from the directory. The ? sign means 1 character.
- **ls name*name** : Gives the content from the directory. The * sign means 0 or more characters.
- ls name\*name\* : Gives the content from the directory. The * sign means 0 or more characters.
- **ls name[[:digit:]]name** : Look for the files in the directories that start with an specific name, then a digit, and end with and specific name.
- **ls name[[:alpha:]]name** : Look for the files in the directories that start with an specific name, then a alphabetic character, and end with and specific name.
- **ls name[[:alnum:]]name** : Look for the files in the directories that start with an specific name, then a alphanumeric character, and end with and specific name.
- **ls name[[:lower:]]name** : Look for the files in the directories that start with an specific name, then a alphabetic lower character, and end with and specific name.
- **ls name[[:upper:]]name** : Look for the files in the directories that start with an specific name, then a alphabetic upper character, and end with and specific name.
- **locate** word : Search in the whole computer the specified word.
- **locate [[:lower:]]** word : Search in the whole computer a word that starts with an alphabetic lower character, and end with and specified name.
- **find** . -name "file name" : Return all the routes where the file mentioned appears.
- **find / -name filename** : The bar means that finds in the source folder.
- **find . -atime +100** : Files that are in a folder, that where open 100 days ago.
- find / -name *.txt -fprint new_file_to_print.txt : Print all the .txt files in a specified new file.
- **stat** file_name : Show the statistics of a file, size, block, access (permissions), modifications, changes.
- **chmod +x file_name** : Give execution permissions to the user, group, global.
- **chmod 0### file_name** : Change the permissions for a specific file.

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

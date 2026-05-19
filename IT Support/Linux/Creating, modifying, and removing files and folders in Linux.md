# Creating, modifying, and removing files and folders in Linux

## Senario
There are three learning objectives for this lab:
1. Creating directories (folders)
2. Moving and deleting files and directories (folders)
3. Searching in files

## 1. Creating directories (folders)
### Senario
In the directory /home/user/Desktop contains a file called "colors". Open the file, and for every line listed in it, create a new folder with that name in the directory /home/user/Documents
<br>

1. Go to the directory
```terminal
cd /home/user/Documents
```

2. Open the colors file
```terminal
cat 
```

3. Create the directories based on the listed name
```terminal
mkdir red blue green yellow magenta
```

## 2. Moving and deleting files and directories (folders)

### 2.1 Moving files and directory
#### Senario 1
In the directory /home/user/Pictures, take all the hidden files and move them into the directory /home/user/Documents/Hidden
<br>

1. Go to Pictures directory
```terminal
cd /home/user/Pictures
```

2. Show the directory contents, including hidden files.
```terminal
ls -a
```

3. Move the hidden files into /home/user/Documents/Hidden
```terminal
mv .apple .banana .broccoli .milk /home/user/Documents/Hidden
```

4. Verify the hidden files had been moved
```terminal
cd ../Documents/Hidden && ls
```

#### Senario 2
In the directory /home/user/Movies, there's a folder called "Europe Pictures". Move this folder into the correct directory for pictures: /home/user/Pictures.
<br>

1. Go to Movies directory and check the folder "Europe Pictures"
```terminal
cd /home/user/Movies && ls
```

2. Move the "Europe Pictures" to /home/user/Pictures.
Note: the use of the backslash "\" to escape the space between "Europe" and "Pictures" in the directory name, "Europe Pictures".
```terminal
mv /home/user/Movies/Europe\ Pictures /home/user/Pictures
```

3. Verify the "Europe Picture" had been moved
```terminal
cd /home/user/Pictures && ls
```

#### Senario 3
Use a "dot" to copy or move files from /home/user/Images/Vacation.JPG to /home/user/Pictures

1. Check the "Vacation.JPG" in /home/user/Pictures or not
```terminal
cd /home/user/Pictures && ls
```

2. Use a "dot" to move the files from /home/user/Images/Vacation.JPG to /home/user/Pictures
```terminal
mv /home/user/Images/Vacation.JPG .
```

3. Verify the "Vacation.JPG" had been move to /home/user/Pictures or not
```terminal
ls
```

### 2.2 Deleting files and directory
#### Senario
Remove the following files and folder from /home/user/Music:
- Best_of_the_90s
- 80s_jams
- Classical
- Rock (folder)


1. Navigate to the Music folder and check the files and folder status
```terminal
cd /home/user/Music. && ls
```

2. Remove the files
```terminal
rm Best_of_the_90s 80s_jams Classical
```

3. Remove the folder
Note: To remove a directory with content, the rm command is used instead of rmdir. The option -r tells the command to remove the directory, along with its content recursively.
```terminal
rmdir Rock
```

4. Verify the files and folder had been remove
```terminal
ls
```

## 3. Searching in files
### Senario
 Find the files that have the word "vacation" in directory /home/user/Downloads then move the files to /home/user/Documents

1. Find files
```terminal
grep -rw /home/user/Downloads -e "vacation"
```

2. Move the files to /home/user/Documents
```terminal
mv /home/user/Downloads/Iceland /home/user/Downloads/Japan /home/user/Documents
```

3. Verify the files had been move
```terminal
cd /home/user/Documents && ls
```

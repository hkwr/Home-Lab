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




### 2.2 Deleting files and directory

 

<font style="color:red">*Brief explanation of .gitignore goes here*</font>

All examples are based on this file tree/structure.
```
repo
├── fruit
│   ├── apple.txt
│   ├── orange.png
│   └── kiwi.mp3
├── animals
│   ├── birds
│   │   ├── kiwi.mp3
│   │   └── pigeon.zip
│   ├── bear.jpg
│   ├── kangaroo.png
│   └── fish.mp4
├── tree.txt
└── README.md
```

### Excluding a File with  .gitignore
To exclude a file, add the file's path in a line. This example excludes the file `tree.txt` located at the root.
```
/tree.txt
```

### Excluding Files that Share Names
To exclude all files with a certain name, add the file's name without any slashes(`/`). This excludes any file with the same name from the repository.

In this example, `/fruit/kiwi.mp3` as well as `/animals/birds/kiwi.mp3` are excluded.
```
kiwi.mp3
```

### Excluding a Directory
Excluding a directory is done by adding the directory name appended with a slash(`/`).
```
fruit/
animals/birds/
```
Alternatively, adding an asterisk(`*`) also works. 
```
animals/*
```

### Comments
All text prepended by the number sign(`#`) is considered as a comment.
```
# This is a comment
```

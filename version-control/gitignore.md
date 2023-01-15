<font style="color:red">*Brief explanation of .gitignore goes here*</font>
`.gitignore` templates can be found [here](https://github.com/github/gitignore).

All examples are based on this file tree/structure.
```
repo
├── fruit
│   ├── banana.txt
│   └── kiwi.mp3
├── animals
│   ├── birds
│   │   ├── kiwi.mp3
│   │   ├── pigeon.html
│   │   ├── pigeon.bmp
│   │   └── pigeon-photos.zip
│   ├── badger.jpg
│   └── fish.mp4
├── tree.txt
└── README.md
```

## Excluding a File with  `.gitignore`
To exclude a file, add the file's path in a line. This example excludes the file `tree.txt` located at the root.
```
/tree.txt
```

## Excluding Files that Share Names
To exclude all files with a certain name, add the file's name without any slashes(`/`). This excludes any file with the same name from the repository.

In this example, `/fruit/kiwi.mp3` as well as `/animals/birds/kiwi.mp3` are excluded.
```
kiwi.mp3
```

## Excluding Files with Names that Share Sections
Adding an asterisk(`*`) to a `.gitignore` entry replaces it with any possible sequence of characters.

For example, **to exclude files with names that start with a certain series of characters**, add the characters followed by an asterisk(`*`).

In this example, the files `/fruit/banana.txt` and `/animals/badger.jpg` are excluded.
```
ba*
```

With this, it is possible to exclude any files with a certain name, regardless of extension. Both lines in the example exclude `/animals/pigeon.html` and `/animals/pigeon.bmp`.
```
pigeon.*
/animals/pigeon.*
```
Notice that this example will not exclude `/animals/pigeon-photos.zip`. The following example, however, includes all three.
```
pigeon*
```

**To exclude files with names that end with a certain series of characters**, we do the reverse. Add an asterisk(`*`) followed by the desired string. The most common use-case is excluding files with a certain extension. Here, `/tree.txt` and `/fruit/banana.txt` are excluded.
```
*.txt
```

## Excluding a Directory
Excluding a directory is done by adding the directory name appended with a slash(`/`).
```
fruit/
animals/birds/
```
Alternatively, including an asterisk(`*`) also works. 
```
animals/*
```

## Comments
All text prepended by the number sign(`#`) is considered as a comment.
```
# This is a comment
```

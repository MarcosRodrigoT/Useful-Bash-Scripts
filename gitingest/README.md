# gitingest

This is my own implementation of [gitingest](https://github.com/cyclotruc/gitingest). It converts an entire directory into a text file containing the project structure, as well as the content from all the files, making it easier to digest for any LLM (ChatGPT, Grok, Gemini, Llama, etc.).

I made this so that I can use it on my local (private) repositories.

## Get started

To run this command, simply:

```bash
gitingest my_project
```

```text
marcos@MARCOS-LAPTOP /tmp $ gitingest my_project/
=========================================================
Project directory structure
=========================================================
my_project/
├── dir1
│   └── file1.txt
└── dir2
    └── file2.txt

3 directories, 2 files

=========================================================
my_project/dir1/file1.txt
=========================================================
This is file 1

=========================================================
my_project/dir2/file2.txt
=========================================================
This is file 2
```

You can also exclude specific sub-directories (useful for directories such as `venv`, `__pycache__`, etc.):

```bash
gitingest my_project/ --exclude dir1,dir2
```

```text
marcos@MARCOS-LAPTOP /tmp $ gitingest my_project/ --exclude dir1,dir2
=========================================================
Project directory structure
=========================================================
my_project/

0 directories, 0 files
```

# git-commands

## CHAPTER - 1
```bash
sudo apt update
sudo apt install git
git --version
cd ~
mkdir git-course
cd git-course/
code .
```

### vscode
```bash
git config --global user.name "kamsofts"
git config --global user.email "kamsofts@gmail.com"
git config --global init.defaultBranch main
git init 
```
README.md file created

## CHAPTER - 2
```bash
touch chapter01.txt
git status
git add README.md
git status
git commit -m "README.md"
git log
git status
```

## CHAPTER - 3
```bash
touch chapter02.txt
git add .
git commit -m "chapter02" 
git log 

#copy hash value for first commit "README.md"
#for me : 6e522a8e99f0df7f97bf496a041c63ec99b5a99f

ls -l 
#output : 3 files

git checkout 6e522a8e99f0df7f97bf496a041c63ec99b5a99f
ls -l 
#output : 1 file

nano README.md 
#modify file, save and exit

git checkout -f main
<<REF_COMMENT
	-f, --force
           When switching branches, proceed even if the index or the working tree differs from HEAD, and even if there
           are untracked files in the way. This is used to throw away local changes and any untracked files or
           directories that are in the way.

           When checking out paths from the index, do not fail upon unmerged entries; instead, unmerged entries are
           ignored.
REF_COMMENT

ls -l
#output : 3 files

git status
```

## CHAPTER - 4
```bash
touch chapter03.txt
git status
git add .
git status
git commit -m "chapter03"
git log
touch chapter04.txt
```
RESTORE
-------
```bash
git status
git add chapter04.txt
git status
git restore --staged chapter04.txt
git status
git commit -m "chapter04"
```

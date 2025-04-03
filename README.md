# kyuhyunp.github.io

## Best Practices
### Minimize context switching
- Send less messages back and forth
- Work on detailed requirement before coding

### Doing pull request well and save time
- Stacking well by dividing up the task in order
- Commit one functionality at a time with 100 lines of edit or less
- Add many unit test cases of about 400 - 500 lines

### Don't approve the code if you are not confident with it

## Terminal guide
### What is `$PATH`
`$PATH` is a environment variable that is file location-related. 
For instance, when you run `make` the terminal looks for `make` in `$PATH`

### Checking `$PATH`
```
echo $PATH
```

### Adding to `$PATH`
```
export PATH=$PATH:<pathname>
```
Current path is connected with a new pathname using :



## Github guide

### How to initialize git after the set up
- Create a new branch and move to the new branch
  ```
  git branch <branch name>
  git checkout <branch name>
  ```

- Check that you are in the new branch
  ```
  git branch
  ```
  
- Delete the "main branch" on github
  ```
  git branch -d <main branch name>
  ```

### How to use .gitignore to exclude files to push
- Create .gitignore if you haven't done so
  ```
  touch .gitignore
  ```

- Edit .gitignore using vi
  ```
  vi .gitignore
  ```

### How to create a pull request
- Pull all the changes
  ```
  git fetch origin
  git merge origin/<main branch name>
  ```
  
- Add all files to push and check
  ```
  git add <file name> 
  git status
  ```
  
- Commit and push the changes (Might have to visit github to get the [password](https://stackoverflow.com/questions/68775869/message-support-for-password-authentication-was-removed))
  ```
  git commit -m <commit message>
  git push
  ```

- Go to github repo to make the pull request

### How to write a pull request
- Make sure to add all the tests you have done
- Include descriptions to share knowledge


### How to view the pull request and the tests within it
1. Go to the commit

![image](https://github.com/user-attachments/assets/7a67a2f2-1390-43ca-b340-48f7ffb4b2dd)

2. Click on the number

![image](https://github.com/user-attachments/assets/1c2f53da-ff1f-4527-ab80-ed6822228b0a)

### How to remove files from github without deleting from your local file system
- For deleting a file
```
git rm --cached file_to_remove.txt 
```
- For deleting a folder
```
git rm --cached -r directory_to_remove
```
- Make sure to add files to .gitignore
- Commit and push
```
git commit -m "<commit message>"
git push
```

### What if .git folder is created in the wrong location
- Move the folder to the correct location
- Run `git rm --cache <filename>` to correct the names

### How to add or remove multiple files
To stage your whole working tree:
```
$ git add -u :/
```

To stage just the current path:
```
$ git add -u .
```


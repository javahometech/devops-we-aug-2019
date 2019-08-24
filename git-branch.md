### Branches in git

- Display local branches 

``` git branch ```


- Display remote branches 

``` git branch -r ```

- Display local and remote branches 

``` git branch -a ```

#### Create Branch and Work on it

Every new implementation/bugfix must be done in a separate branch
- git branch <branch-name>
  example
  ```
    git branch task-1
  
  ```
- Branch is usually created from current branch 
- Breanches are light weight in git

- Switching to task-1 branch
```
  git checkout task-1

```
- Add few commits to task-1

#### Merging changes from your branch to main branch
Typically you cannot merge changes directly to main branch rather it has to be reviewed before you merge changes to main.
- You have to push your local branch to remote ``` git push origin task-1 ```
- Create pull request in Web UI
- After getting approval for pull request merge it. and delete the branch 
- to delete branch ```  git branch -d task-1  ```



#### Fore deleting a branch

Sometimes you comeplete a task and client say we do not need those changes in such scenarios we have to force delete branches

```
   git branch -D <branch-name>
   -D is for force delete
```
- Delete branch in remote
  - First delete branch in local
  - Then run this command ``` git push -d origin task-1 ```
  
 #### Resolving Conflicts (Interview Question)
 
 Conflicts occur when multiple developers working on same file and same line.
 
 Conflicts can be resolved manually or using tools (Ex: DiffMerge Tool)
 
 - Install diffmerge tool
    https://sourcegear.com/diffmerge/downloaded.php
 - Integrating diffmerge with Git place folllowing configurations in ($USER_HOME/.gitconfig) 
 ```
 [diff]
    tool = diffmerge
[difftool "diffmerge"]
    cmd = C:/Program\\ Files/SourceGear/Common/DiffMerge/sgdm.exe \"$LOCAL\" \"$REMOTE\"

[merge]
    tool = diffmerge
[mergetool "diffmerge"]
	keepBackup = false
    trustExitCode = true
    cmd = C:/Program\\ Files/SourceGear/Common/DiffMerge/sgdm.exe -merge -result=\"$MERGED\" \"$LOCAL\" \"$BASE\" \"$REMOTE\"

  ```
  
  - Opening diffmerge tool ``` git mergetool ```
  
#### Git undoing changes
- Discard changes in working area ``` git checkout <file-name1> <file-name2> ```
- Unstage file/files, takes changes form staging and puts it back to working area ``` git reset HEAD <file-name>
- Git Reset
  ``` 
     git reset a96e78c 
     Reset deletes all commits above mentioned commit   
     Use reset only for local commits not for remote commits
  ```
- Different Modes of reset
  - Mixed reset 
    ``` git reset --mixed a96e78c ```
    Default is --mixed, it keeps changes in work area
  - Soft Reset (Interview Question)
    ``` git reset --soft a96e78c ``` keeps changes in index/staging area
  - Hard Reset (Interview Question)
    ``` git reset --hard a96e78c ``` Discards changes premanently
    
 ##### Git Revert (Undo Commit)
 - Git revert undoes changes in specific commit and makes new commit
   ``` git revert commit-id ```

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


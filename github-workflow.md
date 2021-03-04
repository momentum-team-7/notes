# GitHub

[GitHub Guide](https://guides.github.com/introduction/flow/)

## Starting a project
- Everyone on the team does:
```git clone <repo url>```
- The owner of the repo may have to invite teammates in the settings

## Starting work
1. Pull in any recent updates to the `main` branch.
```git checkout main```
```git pull```
2. Create a new branch for the task you are working on. 
```git checkout -b <name-of-branch>```
3. `add`, `commit`, `push` regularly as usual

## Switching between existing branches
If you have multiple branches, you get to the one you want to work on with
```git checkout <name-of-branch>```

## Merging your work with `main`
1. Pull in any recent updates to the `main` branch.
```git checkout main```  
```git pull```  
2. Check out your branch.  
```git checkout <name-of-branch>```  
3. Merge any recent changes from `main` into your branch.  
```git merge main```   
4. If you get a message that you got merge conflicts, go to VS code and fix them.
5. Push the post-merge version of your branch to GitHub.  
```git push```  
*If you see a message that there is no upstream branch, follow the instructions that git gives you in the terminal.*
6. On the GitHub site, click the button to "compare and pull request". This means "I am asking for my code to be merged to the `main` branch.
7. Ask your teammate(s) to review your pull request.
8. *Teammate* checks out your branch on their machine, runs it, and reviews it.
9. *Teammate* leaves feedback on your pull request.
10. *You* respond to feedback, add, commit, and push, and ask for a second review.
11. *Teammate* approves your pull request and merges it on the GitHub site. They delete the branch.
12. *Everybody*  
Update your local version of `main`  
```git checkout main```  
```git pull```  

Either start a new branch with  
```git checkout -b <new-branch>```  

or merge latest changes to the branch you are currently working on  
```git checkout <branch-you-are-working-on>```  
```git merge main```  
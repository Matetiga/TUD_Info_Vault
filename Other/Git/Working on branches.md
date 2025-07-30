## Create a new Branch
```text
git branch branch_name

# to switch into new branch 
git switch branch_name

# this will create and swap into the new branch 
git switch -c branch_name

# to see which branch is currently on 
git branch 
```

---
#### To merge a Branch to main
- change *branch_name* to the actual name 
```txt
# inside branch main
git merge -m "Any_Message" 'branch_name'
```

---
### Delete a branch 
```txt 
git branch -d branch_name
```
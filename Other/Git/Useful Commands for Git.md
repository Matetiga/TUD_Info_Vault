## Ignore files in `.gitignore`
- write inside this file all files you want to ignore (for `git add `)
```txt
# this ignores all files that end with .txt
*.txt

# this ignores all files that contain "Test" in their name
*Test*
```

---

## Remove files from staging 
- to remove files you don't want to commit
`git restore --staged "file_name.txt"`

---
## Remove a file from git 
`git rm "file_name.txt"`
- if you want to recover a file (*that has been previously committed*) 
`git recover "file.name.txt"`


---
## Log of every commit 
`git log`

---
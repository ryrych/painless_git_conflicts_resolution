Example for [Painless Merge Conflict Resolution in Git](http://blog.wuwon.id.au/2010/09/painless-merge-conflict-resolution-in.html)

How to try it out to follow the article?
- `git checkout beta`
- `git merge master`

In short:
- don't rely entirely of `git merge` magic - run `$ git config merge.conflictstyle diff3`
- using visual tools like **meld**, **opendiff* can save your time

## How to generate 3 stages (ours, theirs, and base one)?

`merge.conflictstyle` has to be set to `diff3`

`git merge master`

```
git show :1:roses.txt > roses.common.txt
```
```
git show :2:roses.txt > roses.ours.txt
```
```
git show :3:roses.txt > roses.theirs.txt
```

source: [Pro Git](http://git-scm.com/book/en/v2/Git-Tools-Advanced-Merging#Merge-Conflicts)

Now take a second to look at that diagram and realize what happened: it essentially undid the last git commit command. When you run git commit, Git creates a new commit and moves the branch that HEAD points to up to it. When you reset back to HEAD~ (the parent of HEAD), you are moving the branch back to where it was, without changing the index or working directory. You could now update the index and run git commit again to accomplish what git commit --amend would have done (see Changing the Last Commit).

Note that if you run git status now you’ll see in green the difference between the index and what the new HEAD is.

The next thing reset will do is to update the index with the contents of whatever snapshot HEAD now points to.

let's try to do a pull request!!.

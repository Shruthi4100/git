In Local repository 

git init

touch file1 file2 touch

git add .

git commit -m "1st"

git remote add origin https://github.com/Shruthi4100/git.git

git push

enter the credentials

I have pushed the file created by mistake that is touch. we delete it and push again.

I  added important details in file2 and pushed it

I deleted file2 accidently and deleted it. And even pushed it.

Thanks to git. here we can revert back to previous commit using git revert <commit-id>.

Hence successfully able to revert the commit and got file2 back.And pushed it back to repository.

So to avoid accidental deletions or changes to existing code lets create branches and make code changes and merge it to master.

git checkout -b branch1

lets create file3 and store the code required for testing.

lets create another branch branch2 ( git checkout master --> this will switch to master),( use git branch --> to check in which branch you are)

git checkout -b branch2

git checkout branch1 --> switches to branch1 ( made some code changes to file1)

git checkout branch2 --> swictched to branch2 ( made some code changes to file2)

git checkout branch1 , git merge branch2 ( will merge branch2 to branch1) (the branch1 will have changes both of branch1 & branch2)

git branch -D branch2 ( delete the branch2 as branch1 have changes of branch2) and do git push on branch1

master -> git merge branch1 (merged both master and branch1)

when i did git push it showed some error because of this readme file editing i made in remote repository i solved it by using command --> git merge orgin/master & then git push)

Now lets do some git stashing practice - if we made code update in wrong branch i.e instead of branch1 we made in master then by using git stashing we can transfer the updates made in master to branch1. conditions applied - this can be done only if we didn't commit yet
lets do some code changes in master branch and transfer the changes to branch1

master --> make some changes in file2 and git add ., git stash save , git stash list (copy the stashid (ex- stash@{0}))

git checkout branch1 , git stash apply stash@{0},git add. , git commit -m "stashed changes commit" ( the code changes will be transferred to branch1)





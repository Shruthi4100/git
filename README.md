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

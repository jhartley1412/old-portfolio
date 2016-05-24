May 24, 2016

Alright. So this has happened enough times that I need to write this somewhere so I don't have to go and keep finding it on the internet. Merge conflicts. You getting a bunch of .scssc file conflicts? Delete them: git rm <file name> (http://stackoverflow.com/questions/1380670/how-do-i-fix-a-merge-conflict-due-to-removal-of-a-file-in-a-branch)



How about those super fun DS_Store files? Remember the .gitignore stuff. Show those hidden files: defaults write com.apple.finder AppleShowAllFiles YES (http://ianlunn.co.uk/articles/quickly-showhide-hidden-files-mac-os-x-mavericks/). 

Then delete the DS_Store files:   find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch

and type ".DS_Store" into the .gitignore file (you may have to create it*): git commit -m '.DS_Store banished!'


*git add .gitignore (http://stackoverflow.com/questions/107701/how-can-i-remove-ds-store-files-from-a-git-repository)
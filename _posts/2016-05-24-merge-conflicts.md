---
layout: post
title: "Merge Conflicts"
date: 2016-05-24
---

<h2> It's like, 2am </h2>

Alright. So this has happened enough times that I need to write this somewhere so I don't have to go and keep finding it on the internet. Merge conflicts. You getting a bunch of .scssc file conflicts? 

Delete them: 
<span class="sec-font bg-font"> git rm [file name] </span>

( <a href="http://stackoverflow.com/questions/1380670/how-do-i-fix-a-merge-conflict-due-to-removal-of-a-file-in-a-branch"> http://stackoverflow.com/questions/1380670/how-do-i-fix-a-merge-conflict-due-to-removal-of-a-file-in-a-branch </a> )



How about those super fun DS_Store files? Remember the .gitignore stuff. 

Show those hidden files: 
<span class="sec-font bg-font"> defaults write com.apple.finder AppleShowAllFiles YES </span> 

( <a href="http://ianlunn.co.uk/articles/quickly-showhide-hidden-files-mac-os-x-mavericks/"> http://ianlunn.co.uk/articles/quickly-showhide-hidden-files-mac-os-x-mavericks/ </a> )

Then delete the DS_Store files:   
<span class="sec-font bg-font"> find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch </span>

and type ".DS_Store" into the .gitignore file (you may have to create it*): 
<span class="sec-font bg-font"> git commit -m '.DS_Store banished! </span>


*git add .gitignore ( <a href="http://stackoverflow.com/questions/107701/how-can-i-remove-ds-store-files-from-a-git-repository"> http://stackoverflow.com/questions/107701/how-can-i-remove-ds-store-files-from-a-git-repository </a> )


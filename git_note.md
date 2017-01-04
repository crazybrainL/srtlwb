# Git Note
 * [Git Submodul](http://blog.chh.tw/posts/git-submodule/)
 * [How do I remove a submodule?](http://stackoverflow.com/questions/1260748/how-do-i-remove-a-submodule)

-----

#### To remove a submodule you need to:
 - Delete the relevant section from the .gitmodules file.
 - Stage the .gitmodules changes git add .gitmodules
 - Delete the relevant section from .git/config.
 - Run git rm --cached path_to_submodule (no trailing slash).
 - Run rm -rf .git/modules/path_to_submodule
 - Commit git commit -m "Removed submodule <name>"
 - Delete the now untracked submodule files: rm -rf path_to_submodule


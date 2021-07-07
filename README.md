# wikiTests
Testing putting the wiki in /docs/ as a subtree


Steps to add the wiki to your project as a sub folder: (in this case we will use `/docs/`) 

Description | Command
--- | ---
Create a working directory of your project | `git clone git@github.com:MagikEh/wikiTests.git`
Add a subtree into the target directory | `git subtree add  --squash --prefix docs git@github.com:MagikEh/wikiTests.wiki.git master`

git subtree pull --squash --prefix docs git@github.com:MagikEh/wikiTests.wiki.git master
git push

--changes--

git commit -m "Changes have been made, beware."
git subtree push --prefix docs git@github.com:MagikEh/wikiTests.wiki.git master
git push

--To update docs with changes from the wiki--
git subtree pull --squash --prefix docs git@github.com:MagikEh/wikiTests.wiki.git master
git push

**Caveats:
- Changes made in the web gui must be pulled and squashed into the main project main branch 
  (changes in sub branches are not visible on the wiki)

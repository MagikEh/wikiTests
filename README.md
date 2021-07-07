# wikiTests
---
Testing putting the GitHub wiki in the /docs/ as a subtree of the main project. Steps are as follows:

Description | Command
--- | ---
Create a working directory of your project | `git clone git@github.com:MagikEh/wikiTests.git`
Add a subtree into the target directory (`/docs/`) | `git subtree add  --squash --prefix docs git@github.com:MagikEh/wikiTests.wiki.git master`
Grab any existing wiki pages and stuff them into the `/docs/` folder | `git subtree pull --squash --prefix docs git@github.com:MagikEh/wikiTests.wiki.git master`
Sync the main project with our local changes | `git push`
⠀|⠀
make changes to the project | `sed -i 's/foo/fuzz/g' *`
⠀|⠀
Commit changes to main branch | `git commit -m "Changes have been made, beware."`
Push commits to the main branch | `git push`
Push relevant commits to the subtree's master branch | `git subtree push --prefix docs git@github.com:MagikEh/wikiTests.wiki.git master`
⠀|⠀

It is recommended that you only edit the wiki from a single source (ie: changes to `/docs/`) as changes to the wiki from the web interface will commit them directly to the wiki's git. Changes will then have to be pulled and merged into the subtree to bring things back into sync. If for whatever reason you do need to synchronize the wiki subtree with the main project's main branch you can follow the below steps:

```
$ git subtree pull --squash --prefix docs git@github.com:MagikEh/wikiTests.wiki.git master
$ git push
```

**Caveats:**
- Changes made in the web gui must be pulled and squashed into the main project main branch 
  (changes in non-main branches of the subtree are not visible on the web wiki)
- The wiki is presented to users over the web as a flat website (no sub-directories) so file names ought be unique in order to prevent confusion.
- Making changes to the main project's main branch `/docs/` will have no effect on the web view until changes are pushed to the .wiki subtree.
- "I don't want to squash all my commits", too bad. 
   - It seems that git won't attempt to merge changes after pulling and fails out if you don't add the squash option. Fix: Don't make changes to the wiki from the web.
- For whatever reason the wiki defaults to using 'master' as the main branch name, rename if you feel necessary.  



**Credits:**
- Check out this awesome example of localization by Archi [Steam card idler](https://github.com/JustArchiNET/ArchiSteamFarm/wiki). (clone the wiki and checkout the folder structure)
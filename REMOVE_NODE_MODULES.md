# PR: Remove tracked node_modules and ensure .gitignore

Summary
- Remove the committed node_modules directory to reduce repository size and restore proper package management practices.

Why
- Committed node_modules bloats the repository, makes PRs/merges slow, and is unnecessary because dependencies are declared in package.json.

What to do locally (copy/paste)
1. git checkout -b remove-node_modules
2. git rm -r --cached node_modules
3. git commit -m "chore: remove node_modules from repository; ensure .gitignore excludes node_modules"
4. git push origin remove-node_modules

After you've pushed the commit to this branch, the PR will contain the removal commit for review and merge. This change only affects the repository's tracked files — it does not delete anyone's local node_modules directories.

Notes
- Please run `npm install` or `yarn install` after merging to restore local node_modules.
- If you want me to handle any part of this process differently, reply with instructions.

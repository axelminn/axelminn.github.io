---
name: push
description: Push the personal page to GitHub. Use whenever the user asks to push, publish or deploy the site. First brings CLAUDE.md up to date with the changes being pushed, then commits and pushes.
---

# Push the site

Run these steps in order from `/home/axel/claude/personal-page`.

1. Run `git status --short` and `git diff HEAD --stat`, plus `git log origin/main..HEAD --oneline`, to see what is about to be pushed. If there is nothing to commit and nothing unpushed, say so and stop.
2. Read `CLAUDE.md` and compare it with those changes. Update it wherever it has gone stale: files added or removed, sections renamed or reordered, new styling tokens or breakpoints, changed script behavior, deployment changes. Keep edits small and in the file's existing style. If nothing is stale, leave it alone and say so.
3. `CLAUDE.md` is public once pushed. Do not add secrets, tokens or private details to it. Check the diff for any before committing.
4. Stage the specific changed files (not `git add -A` blindly) and commit with a short, imperative message. End it with the Co-Authored-By line from the session's attribution reminder. Include the `CLAUDE.md` update in the same commit, or in a separate "Update CLAUDE.md" commit if the code change is unrelated.
5. Run `git push origin main`. If it fails on authentication, tell the user to run `gh auth status` or `gh auth login` and stop. Never force-push.
6. Report what was pushed, whether `CLAUDE.md` changed, and the live URL: https://axelminn.github.io/ (updates in about a minute).

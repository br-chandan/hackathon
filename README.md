# Hackathon Repository

This repository contains a simple polyglot project skeleton for a hackathon.

Structure
- `frontend/` - UI or front-end code (React, Vue, static site, etc.)
- `backend/` - Server or API code (Node/Express, Python/Flask, etc.)
- `plans/` - Project plans, notes, designs
- `drafts/` - Drafts, prototypes, experimental files

.gitignore behavior
- The `.gitignore` at the repository root applies recursively to files and directories in subfolders.
- Patterns without a leading slash (e.g. `node_modules/`) will match locations anywhere in the repo.
- Patterns starting with a leading slash (e.g. `/dist/`) are anchored to the repository root.
- Files already tracked by Git will not be ignored until you stop tracking them (use `git rm --cached <file>`).

Initial commit
- This repo has an initial commit with this README and the `.gitignore`.

Next steps
- Initialize `frontend` and `backend` with your chosen frameworks. I can scaffold `package.json`, `requirements.txt`, or starter apps if you want.

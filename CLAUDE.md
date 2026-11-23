# SimpleCal — Project Instructions for Claude

Single-file, mobile-first meal/kcal checklist (`index.html`, no backend, no build step, data in `localStorage`). See [README.md](README.md) for design principles, data model and deploy steps.

## Dev Support Folder
Path: D:\Claude AI Projects\projects\Personal Dev Support Folder\
Relevant sections for this project: 06-reference-library (patterns), 07-templates-snippets (small single-file web app scaffolding), 08-meta-ai-roles (role selection)
Autonomy: follow this folder's own autonomy default (see its README) for any in-folder work.
Write-back: if something reusable comes up while working here (a checklist, a fix that generalizes, a pattern that'd repeat elsewhere), write it into the support folder as it happens — don't wait to be asked. See the support folder README's "Build philosophy" section for what counts as reusable.
Roles: auto-select the right role(s) from the task itself, using 08-meta-ai-roles/ai-role-cheatsheet.md and ai-role-workflow-cheatsheet.md — don't wait to be told which hat to wear. State which hat you're wearing if it's not obvious, but don't ask permission to wear it. Multiple hats can apply to one task; wear them in sequence or name the tension explicitly rather than silently picking one and hiding a conflict.

## Project notes
- All meals, kcal values and goals live in the `CONFIG` block at the top of the script in `index.html` — edit there, not scattered through the markup.
- kcal is computed at read time, so changing a config value also changes history. Keep that in mind before editing existing item kcal.
- Repo stays private unless the owner raises otherwise.

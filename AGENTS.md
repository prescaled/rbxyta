# Shared Obsidian vault

This vault is shared by Rivin and Prescaled through https://github.com/prescaled/rbxyta.

The default Miro board for ROOM 0 is https://miro.com/app/board/uXjVEVisZSo=/. Use this board for future game notes and mind maps unless the user specifies another destination. It replaces the previously used board ending in `uXjVEVjFuGU=`.

- Keep notes and their supporting attachments synced to the shared GitHub repository. The user has authorized committing and pushing vault changes so Prescaled can access them.
- Before editing any vault file, always pull the latest version from GitHub and successfully integrate remote changes. If the pull fails or conflicts remain, resolve the sync issue before editing; do not proceed with stale files. Fetch and integrate remote changes again before pushing. Preserve local edits and both collaborators' work when resolving conflicts. Never force-push or discard notes to resolve a sync problem.
- After completing requested note changes, commit and push the relevant notes and attachments to the shared `main` branch. Verify the push succeeded; if authentication, network access, or conflicts prevent syncing, report that explicitly.
- Preserve unrelated local changes. Do not include credentials, local workspace state, or installed plugin code in note commits.
- Use the repository's configured Git author identity; do not replace it with an invented identity.

Obsidian Git is configured locally for five-minute commit-and-sync, five-minute pulls, and pulling on startup. Its per-device settings are ignored by Git; collaborators configure their own automatic sync settings.

## Building ROOM 0 (Claude and Codex at the same time)

Prescaled works with Claude and Rivin works with Codex. Both use Blender MCP and Roblox Studio MCP. Before any modelling or Roblox Studio work, read and follow `ROOM 0/Production/Collaboration Workflow.md`, `ROOM 0/Production/Art Bible.md` and `ROOM 0/Production/Work Board.md`:

- Only edit areas, files and Roblox folders that your side owns on the Work Board. Claim new items there and push the claim before starting.
- Reuse shared models (Roblox Packages and the shared Blender library); never make a second version of an existing shared model.
- Follow the Art Bible's scale, naming, budget and export rules.


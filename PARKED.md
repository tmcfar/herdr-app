# PARKED — not maintained, may never be implemented

Parked by Tom on 2026-11-10. Tom moved to the stock herdr-app build; this branch is kept only for
reference.

What is here, on top of upstream `master` at 0ac92e4 (2026-11-10):

- `feat: support local machines in wsl` (hayatosc): the app runs its local machine inside a WSL
  distribution, with a WSL picker in Settings.
- `ci(pilot): non-updating Windows build of the WSL branch`: `.github/workflows/pilot-build.yml`,
  a Windows build without self-update. It triggers only on pushes to `pilot`, not on this branch.
- `feat(pilot): Ctrl+wheel zooms the app`.
- `feat(pilot): offer Use Windows instead when the WSL core cannot connect`.

State when parked: CI passed on Windows and Linux; macOS did not run (no runner). The pilot
Windows build passed (run 42872916750). The pre-rebase branch is tag `pilot-pre-rebase-20261110`.

Reviving it means rebasing onto current upstream `master`; expect conflicts in `src/terminal.rs`,
`src/mods.rs`, `src/setup.rs`, `src/programs.rs` and `defaults/mods/files/main.js`.

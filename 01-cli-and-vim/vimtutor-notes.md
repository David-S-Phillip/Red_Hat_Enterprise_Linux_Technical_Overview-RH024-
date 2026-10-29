# Vimtutor Quick Reference & Modal Editing Notes

Notes and keyboard shortcuts compiled from completing interactive `vimtutor` practice sessions on Red Hat Enterprise Linux.
To start vimtutor go to terminal and type 'vimtutor'
---

* **Normal Mode:** Default navigation and command execution mode. Press `Esc` to return here from any other mode.
* **Insert Mode:** Text editing mode. Press `i` to enter Insert mode before the cursor, or `a` to append after the cursor.
* **Command-Line Mode:** Used for saving, exiting, and editor settings. Initiated by typing `:` from Normal mode.

## 2. Editing and text manipulation
* `x` — Delete the character under the cursor.
* `dw` — Delete from the cursor position to the start of the next word.
* `r` — Replace the single character under the cursor with another character.
* `cw` — Change word (deletes from cursor to word end and enters Insert mode).

## 3. Searching and file operations
* `/pattern` — Search forward for `pattern` (press `n` for next match, `N` for previous).
* `?pattern` — Search backward for `pattern`.
* `:w` — Save changes to disk (write).
* `:q` — Quit Vim (fails if unsaved changes exist).
* `:wq` — Save changes and quit Vim.
* `:q!` — Force quit without saving changes.
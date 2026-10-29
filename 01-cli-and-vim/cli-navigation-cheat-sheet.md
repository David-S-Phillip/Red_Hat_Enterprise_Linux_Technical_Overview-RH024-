# Linux CLI Navigation & File System Management Cheat Sheet

Fundamental Linux command-line navigation, file operations, and directory management reference notes compiled during the Red Hat Enterprise Linux Technical Overview (RH024) course.

---

| Command | Description | Example           |
| :--- | :--- |:------------------|
| `pwd` | Print working directory (shows current absolute path) | `pwd`             |
| `cd <path>` | Change directory to specified path | `cd student_work` |
| `cd` or `cd ~` | Navigate directly to user's home directory | `cd ~`            |
| `cd ..` | Move up one level to parent directory | `cd ..`           |
| `cd -` | Switch back to the previous working directory | `cd -`            |

---

## 2. File & Directory Inspection

* **`ls`** — List directory contents.
    * `ls -l` — Detailed long-format listing (permissions, owner, size, modification date).
    * `ls -a` — Show all files including hidden files starting with `.`.
    * `ls -la` / `ls -lh` — Human-readable sizes combined with hidden files and long listing.
* **`cat <file>`** — Display complete contents of a file to stdout.
* **`less <file>`** — View file contents interactively with scrolling page navigation (`q` to exit).
* **`head -n <N> <file>`** — Display first $N$ lines of a file (defaults to 10).
* **`tail -n <N> <file>`** — Display last $N$ lines of a file.
    * `tail -f /var/log/messages` — Monitor log file additions in real time.

---

## 3. Creating, Copying, Moving & Deleting

### Directories
* `mkdir <dir_name>` — Create a new directory.
* `mkdir -p path/to/nested/dir` — Create parent directories as needed without throwing errors.
* `rmdir <dir_name>` — Remove an empty directory.

### Files & Directories
* `touch <file_name>` — Create an empty file or update access timestamp.
* `cp <src> <dest>` — Copy file from source to destination.
    * `cp -r <src_dir> <dest_dir>` — Copy directory recursively including all sub-files.
* `mv <src> <dest>` — Move or rename a file/directory.
* `rm <file>` — Remove a file.
    * `rm -r <dir>` — Remove a directory and its contents recursively.
    * `rm -rf <dir>` — Force recursive deletion without prompting (use with extreme caution).

---
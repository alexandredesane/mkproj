mkproj
======

A tiny CLI tool to create folders and empty files from a simple indented text tree.

Built for web developers who like simple tools, no boilerplate,
and full control over their workflow.


WHY MKPROJ?
-----------

If you often write project structures like this:

my-app/
  index.html
  styles.css
  app.js
  assets/
    icon.png

…and then manually create folders and files one by one,
mkproj is for you.


WHAT IT DOES
------------

- Reads a simple indented text file (.txt)
- Creates directories (mkdir -p)
- Creates empty files (touch / : > file)
- Prints exactly what it is doing in the terminal
- Works without Node, npm, Python or dependencies


PHILOSOPHY
----------

- Text is the source of truth
- Indentation defines hierarchy
- No configuration files
- No project generators
- One job, done well


PLATFORM
--------

- macOS (tested with default macOS Bash)
- Linux may work but is not the main target
- Windows is not supported

This tool is intentionally opinionated.


INSTALLATION
------------

1. Create the command file:

mkdir -p ~/.local/bin
nano ~/.local/bin/mkproj

Paste the script content into the file.

2. Make it executable:

chmod +x ~/.local/bin/mkproj

3. Ensure ~/.local/bin is in your PATH:

For zsh (default on macOS):

export PATH="$HOME/.local/bin:$PATH"


USAGE
-----

Create files and folders from a tree file:

mkproj tree.txt

Preview what will be created (dry run):

mkproj --dry-run tree.txt

Force indentation size (2 or 4 spaces):

mkproj --indent 2 tree.txt

Read from standard input:

cat tree.txt | mkproj -


TREE FILE FORMAT
----------------

Rules:

- Directories must end with a slash (/)
- Use spaces only (no tabs)
- Indentation must be consistent (2 or 4 spaces)
- Comments can be added using #

Example tree.txt:

client-tracker/
  index.html
  styles.css
  app.js
  db.js
  sw.js
  manifest.webmanifest
  icons/
    icon-192.png
    icon-512.png


LICENSE
-------

MIT License.
Use it, modify it, ship it, sell it.
No warranties.


AUTHOR
------

Made by a web developer who prefers:
- local tools
- small scripts
- shipping fast
- owning their workflow


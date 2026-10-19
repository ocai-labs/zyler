# The `zyler` command-line tool

The desktop app includes a CLI for working with a local vault from a terminal or
an external tool. The app does not need to be running. An external tool using the
CLI gets the file access you give it; review its commands before allowing writes.

## Install the command

In Zyler, open **Settings → General → Command line tool** and click **Install**.
Follow any permission prompt, then open a new terminal.

```sh
zyler --version
zyler --help
zyler vaults
```

`vaults` lists vaults the desktop app has opened. Create or open a vault in the app
first. Use `--vault` to name the intended vault explicitly; quote paths containing spaces.

## Read and search

Replace `/path/to/My vault` with your vault path. On Windows, a quoted path such as
`"C:\Users\you\Documents\My vault"` works instead.

```sh
zyler --vault "/path/to/My vault" ls
zyler --vault "/path/to/My vault" search "project"
```

Copy a note id from the listing, then replace `<note-id>` below:

```sh
zyler --vault "/path/to/My vault" cat <note-id>
```

`cat` prints the note as Markdown. In your shell, you can redirect that output to
a `.md` file. Take care with `>`: the shell overwrites an existing destination file.

## Create a note from Markdown

From a local copy of this public repository:

```sh
zyler --vault "/path/to/My vault" new "Weekly review" --body "templates/weekly-review.md"
```

This creates a new note and prints its id. The Markdown file is an input file;
subsequent edits in Zyler do not change it.

## Editing and automation

Use built-in help for the exact options supported by your installed version:

```sh
zyler cat --help
zyler new --help
zyler edit --help
zyler write --help
zyler doctor --help
```

For structured reads, add `--json`, for example:

```sh
zyler --vault "/path/to/My vault" --json ls
```

Read the current note and use the revision checks described in command help before
automating edits. Keep a backup before running a batch of write commands. Use CLI
content commands rather than rewriting `.zyler.json` files yourself.

If the command is not found, reopen your terminal and check the install status in
Settings → General. See [troubleshooting](troubleshooting.md) for more help.

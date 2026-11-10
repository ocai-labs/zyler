# The `zyler` command-line tool

The desktop app includes `zyler`, a command for reading and changing a local vault from a
terminal, a script, or an AI assistant. The app does not need to be running. When it is,
the app and the command share a write lock, so neither overwrites the other.

An external tool using the CLI gets the file access you give it; review its commands before
allowing writes.

## Install the command

In Zyler, open **Settings → General → Command line tool** and click **Install**. Follow any
permission prompt, then open a new terminal and check it:

```sh
zyler --version
```

```text
zyler 0.18.0
commit  6e00cdf28e86, built 2026-11-03T11:43:29.938Z
```

## Choose a vault

Most commands work on one vault. `zyler` uses the first of these it finds:

1. `--vault "/path/to/My vault"` on the command line.
2. The `ZYLER_VAULT` environment variable.
3. The vault folder you are in, or any folder above it.

The simplest way is to open a terminal in the vault folder:

```sh
cd "/path/to/My vault"
zyler ls
```

To see the vaults the app has opened, most recent first:

```sh
zyler vaults
```

`vaults` only lists them; name the one you mean with `--vault` or `cd`. Quote paths that
contain spaces. On Windows, a path such as `"C:\Users\you\Documents\My vault"` works.

## Name a note

Commands take a note by its id, such as `note_osk58obce0sd`, or by its whole title, such as
`"Project plan"`. Reading commands also accept part of a title. If a name matches no note,
or more than one, nothing happens and the command lists the matches so you can use an id:

```text
"e" matches 2 notes. Use an id instead:
  note_osk58obce0sd  Project plan
  note_wow31iq9tdc7  Weekly review
```

## Get help

```sh
zyler --help              # every command
zyler cat -h              # one command, short
zyler cat --help          # one command, in full
zyler help markdown       # the Markdown the CLI reads and writes
```

Next: [read and search](cli-read.md).

# Use with an AI assistant

Zyler has no built-in AI. Instead, a coding assistant that runs commands, such as Claude Code
or Codex, can read and write your notes through the `zyler` command. It works whether or not
the app is open.

## Set it up

1. [Install the command](cli.md#install-the-command).
2. Start the assistant in your vault folder, or set `ZYLER_VAULT` to the vault's path, so
   every command finds the right vault.
3. Tell the assistant about the tool. For example:

```text
My notes are in a Zyler vault. Use the `zyler` command to work with them; run
`zyler --help` first. Read a note with `zyler cat` before changing it, change parts
with `zyler edit` or `zyler block-insert` rather than `zyler write`, and add `--json`
when you need to parse the output.
```

## Keep control of what it changes

- Let the assistant run reading commands freely, and approve writes one at a time until you
  trust its pattern. Most assistants let you allow `zyler cat`, `zyler ls`, and
  `zyler search` while asking about the rest.
- Every write keeps the note's previous state in its version history, so you can restore a
  page from the app.
- Before a large batch of changes, [back up the vault](local-vaults.md#back-up-a-vault).
- A note locked in the app cannot be changed from the CLI.

## Avoid overwriting newer edits

If you edit a note in the app while the assistant works on it, the assistant's next write
could undo your edit. Ask it to pass `--rev`:

1. Read with `--json`. `cat`, `blocks`, and `block` report the note's `repositoryRevision`.
2. Pass that value on the write: `zyler edit "Project plan" --old … --new … --rev <revision>`.
3. If the note changed in between, nothing is written and the command exits with code 5:
   `Note "note_osk58obce0sd" changed before the mutation could apply.` The assistant should
   read the note again and redo its change.

## Calling it from a program

Start `zyler` directly with its arguments, without a shell, for example
`spawn("zyler", ["cat", "Project plan"])`. Going through `cmd /c` or a shell option can split
or run characters such as `&`, `|`, and `>` in titles. See
[doctor and exit codes](cli-troubleshooting.md) for what each exit code means.

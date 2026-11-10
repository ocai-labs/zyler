# Doctor and exit codes

## Check the install and the vault

```sh
zyler doctor
```

`doctor` checks that the command is installed correctly, that the vault's files can be read,
and that the vault's write lock is the one the app uses. Each line says `ok`, `warn`, or
`fail` with a reason. It exits with code 11 when a check fails; warnings alone exit 0.

## The command is not found

Install it from **Settings → General → Command line tool**, then open a new terminal. If the
app reports a conflicting command or a permission error, keep that message and
[contact support](../SUPPORT.md).

## Exit codes

| Code | Meaning | What to do |
| --- | --- | --- |
| 0 | Done | |
| 1 | Unexpected failure | Report it; run again with `ZYLER_DEBUG=1` for details |
| 2 | Bad arguments | Check the command with `zyler <command> -h` |
| 3 | No vault found | Use `--vault`, `ZYLER_VAULT`, or `cd` into the vault; `zyler vaults` lists them |
| 4 | The note matched nothing, or more than one | Use the note's id from `zyler ls` |
| 5 | Someone else wrote first | Read the note again and redo the change |
| 6 | The note is locked | Unlock it from the note's **⋯** menu in the app |
| 7 | The edit was refused | Check block ids and that `--old` matches `zyler cat` exactly |
| 8 | The write may or may not have happened | Read the note before trying again |
| 9 | The history snapshot failed, so nothing was written | Check free disk space and try again |
| 10 | A file is unreadable, or was made by a newer Zyler | Update Zyler; do not recreate the file |
| 11 | `doctor` found a failing check | Read the `fail` lines |
| 12 | The vault is read-only here | Reads still work; check folder permissions |
| 13 | Another program holds the note file | Try again in a moment |

With `--json`, every outcome, including errors, is one JSON object with an `ok` field.

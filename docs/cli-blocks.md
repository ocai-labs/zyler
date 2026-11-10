# Edit inside a note

These commands change part of a note and leave the rest as it is. Block ids come from
`zyler blocks`; see [read and search](cli-read.md#see-a-notes-blocks).

## Find and replace

```sh
zyler edit "Project plan" --old "Draft the outline" --new "Draft the outline for Sync"
```

```text
edited note_osk58obce0sd (1 edit, 1 block)
```

Copy `--old` exactly as `zyler cat` printed it, including Markdown such as `<b>`. If it
matches nothing, nothing is written. By default one occurrence is replaced:

- `--all` replaces every occurrence.
- `--block <id>` looks only inside one block.
- `--edits` takes up to 50 replacements as a JSON array, applied all together or not at all:
  `--edits '[{"oldStr":"draft","newStr":"final"}]'`.

## Insert blocks

`block-insert` reads Markdown from standard input, or from a file with `--body`. `--at` says
where it goes: `end` (the default), `before:<id>`, or `after:<id>`.

```sh
echo "- Add screenshots" | zyler block-insert "Project plan" --at after:TddkAhJJ
```

```text
inserted note_osk58obce0sd (1 block)
```

`--depth 1` nests the inserted blocks one level deeper.

## Change a block

`block-update` changes a block's type or attributes with a JSON object. To tick a task:

```sh
zyler block-update "Project plan" t6Yc_-hS --set '{"checked":true}'
```

```text
updated note_osk58obce0sd (t6Yc_-hS)
```

## Move blocks

```sh
zyler block-move "Project plan" HGT6GXvW --before oKABYuaq
```

```text
moved note_osk58obce0sd (1 block before oKABYuaq)
```

Use `--after <id>` to place them after a block instead. You can name up to 200 blocks.

## Delete blocks

```sh
zyler block-delete "Project plan" 7TWmUygS
```

```text
deleted note_osk58obce0sd (1 block)
```

## On Windows

JSON typed on the command line, as in the examples above, works only in shells such as bash
and zsh; PowerShell and `cmd.exe` split it apart. On Windows, save the JSON in a file and
pass the file instead: `--set "@change.json"` or `--edits "@edits.json"`.

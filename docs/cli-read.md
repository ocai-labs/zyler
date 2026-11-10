# Read and search

Reading never changes the vault. The examples run in a terminal opened in the vault folder;
see [choose a vault](cli.md#choose-a-vault).

## List notes

```sh
zyler ls
```

```text
note_osk58obce0sd  Project plan
note_wow31iq9tdc7  Weekly review
```

Name a note to list only its direct children:

```sh
zyler ls "Project plan"
```

`ls` shows 100 notes at a time. Add `--all` for the whole vault, or `--limit` and the
`--cursor` it prints to page through.

## Search

```sh
zyler search outline
```

```text
note_osk58obce0sd  Project plan
    …s Ship the help center Write the CLI guides Tasks Draft the outline Pick a docs site
```

Search looks in titles and bodies and shows up to 20 hits; `--limit` changes that.

## Print a note

```sh
zyler cat "Project plan"
```

```text
## Goals

- Ship the help center
- Write the CLI guides

## Tasks

- [ ] Draft the outline
- [x] Pick a docs site
```

`cat` prints Markdown in the same form every writing command accepts. To save it as a file,
redirect it: `zyler cat "Project plan" > plan.md`. The shell overwrites an existing file
with `>`.

## See a note's blocks

Each paragraph, heading, list item, and other block has an id. Editing commands use these ids.

```sh
zyler blocks "Project plan"
```

```text
oKABYuaq  heading     Goals
TddkAhJJ  bulletList  Ship the help center
F4YyvQo3  bulletList  Write the CLI guides
HGT6GXvW  heading     Tasks
t6Yc_-hS  taskList    Draft the outline
7TWmUygS  taskList    Pick a docs site
```

Show one block in full:

```sh
zyler block "Project plan" t6Yc_-hS
```

```text
t6Yc_-hS  taskList
- [ ] Draft the outline
```

## Output for programs

Add `--json` before or after the command to get one JSON object on every outcome, errors
included:

```sh
zyler --json ls
```

```json
{
  "ok": true,
  "vault": { "root": "/path/to/My vault", "source": "cwd-ancestor" },
  "notes": [
    { "noteId": "note_osk58obce0sd", "title": "Project plan", "parentId": null,
      "updatedAt": "2026-11-10T10:25:04.383Z", "locked": false }
  ],
  "total": 1
}
```

`cat`, `blocks`, and `block` also report the note's `repositoryRevision`, which keeps an
edit from overwriting a newer one; see [use with an AI assistant](cli-assistants.md).

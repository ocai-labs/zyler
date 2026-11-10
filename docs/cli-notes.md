# Create and change notes

Each write keeps the note's previous state in its version history first, so a change made
from the CLI can be undone in the app.

## Create a note

```sh
zyler new "Project plan"
```

```text
note_osk58obce0sd
created note_osk58obce0sd Project plan
```

The first line is the new id, on its own, for scripts. Add content from a Markdown file, or
put it under another note:

```sh
zyler new "Weekly review" --parent "Project plan" --body review.md
```

`--body -` reads the Markdown from standard input instead of a file:

```sh
echo "Notes from the weekly review." | zyler new "Weekly review" --body -
```

Without `--body`, the note is empty.

## Replace a note's body

```sh
zyler write "Project plan" --body plan.md
```

```text
wrote note_osk58obce0sd 6 blocks
```

`write` replaces everything below the title. To change part of a note, use
[edit inside a note](cli-blocks.md) instead. An empty body is refused for a note that has
content, unless you add `--allow-deleting-content`.

## Rename

```sh
zyler rename "Weekly review" "Weekly review, week 46"
```

```text
renamed note_wow31iq9tdc7 to "Weekly review, week 46"
```

## Move

`--parent` is required: a note's new parent, or `root` for the top level. `--before` places
it in front of a sibling; without it, the note goes last.

```sh
zyler mv "Weekly review, week 46" --parent "Project plan"
zyler mv "Weekly review, week 46" --parent root
```

## Delete and restore

`rm` moves a note and everything under it to the trash, where the app's Trash also shows it.

```sh
zyler rm "Weekly review, week 46"
zyler restore "Weekly review, week 46"
```

```text
trashed note_wow31iq9tdc7
restored note_wow31iq9tdc7 "Weekly review, week 46"
```

## Markdown

The CLI writes the same Markdown that `zyler cat` prints: headings, lists, task lists,
tables, code, callouts, toggles, and more. Bold is written `<b>text</b>`; `**text**` works
too. Run `zyler help markdown` for every form.

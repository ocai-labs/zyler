# Database rows

Create databases and their properties in the app; see [databases](databases.md). From the
CLI you can read rows and set their properties. Each row is a page directly under the
database page, so `zyler ls` and `zyler cat` work on rows like on any other note.

## Read a row

`zyler cat` prints a row's properties as frontmatter at the top, followed by its body.

```sh
zyler ls "Launch plan"          # the rows of a database page
zyler cat "Fix the login bug"   # one row, with its properties
```

## Set properties

Write each property as its own argument. After `=` comes the value as `zyler cat` prints it:
text, a number, a date such as `2026-11-20` (or `2026-11-20/2026-11-22` for a range), or
one option of a select or status.

```sh
zyler set "Fix the login bug" Status=Done Due=2026-11-20
```

After `:=` comes JSON, for lists, numbers, true or false, and clearing a value:

```sh
zyler set "Fix the login bug" Tags:='["Sync","Desktop"]' Shipped:=true Notes:=null
```

JSON typed this way works in shells such as bash and zsh. PowerShell and `cmd.exe` can split
it apart; on Windows, run these from Git Bash or WSL, or from a program that passes each
argument directly (see [calling it from a program](cli-assistants.md#calling-it-from-a-program)).

- Only the properties you name change; the title and body stay as they are.
- Everything is written or nothing is. An unknown property or option is refused with the
  list of valid ones.
- A select option that does not exist is added only if the database allows new options.
  Status options are never added from the CLI.
- Title, Created time, and Last edited time cannot be set. Rename a row with
  `zyler rename`.

# Your local vault

A vault is a folder you choose. Local note creation, editing, and navigation work
without an account. Keep the folder somewhere your user account can read and write.

## What is in the folder?

```text
My vault/
├── notes/          Rich note files (.zyler.json)
├── attachments/    Files attached to notes
└── .zyler/         Vault metadata, history, chat data, and supporting files
```

Some folders appear only after the corresponding feature is used. Enable hidden
files in your file manager to see `.zyler`.

The note's JSON title is authoritative. Its filename includes a permanent note id;
rename notes inside Zyler so the title and filename stay consistent. The sidebar's
page hierarchy is stored in note data rather than a matching tree of folders.

Zyler uses JSON to preserve rich editor content. Markdown is an interchange format:
use [import/export](import-export.md) or the [CLI](cli.md) to work with Markdown.

## Back up a vault

1. Close Zyler windows using the vault and stop any CLI tools writing to it.
2. Copy the **entire vault folder**, including attachments and the hidden `.zyler` folder,
   to your backup destination.
3. Keep more than one backup and check that you can restore a copy.

Version history helps recover individual note edits, but is not a substitute for a
separate backup. Sync is not a substitute for a backup either.

To restore, copy the backup to a folder on disk and choose **Open existing vault**
in Zyler. Use a separate location when checking a backup so you can compare it with
the original before replacing anything.

## What stays on this device?

Window state, indexes, account session data, and other device settings live in the
app's local data directory rather than the vault. Copying the vault does not copy
your sign-in session or every application preference.

## Compatibility messages

If Zyler says a vault or note needs a newer version, update the app. Do not edit
version fields to bypass the check. A newer editor schema may make a note read-only;
open it with a compatible app before editing.

See [privacy](privacy.md) for connected features and [troubleshooting](troubleshooting.md)
for files that do not open.

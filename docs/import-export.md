# Import and export

Zyler stores rich notes as JSON and exchanges content with other tools through
Markdown. Importing a Markdown file creates or adds content to a Zyler page; it
does not turn the original Markdown file into a live vault note.

## Import a file

1. Open the destination vault in Zyler.
2. Go to **Settings → Import**.
3. Choose **Text & Markdown** for `.md`, `.markdown`, or `.txt`, or **HTML** for
   `.html` and `.htm` files.
4. Choose the file, select an import location, and click **Continue**.
5. Review the imported page, especially links, tables, and formatting.

You can also drop a Markdown file onto the Markdown drop area in Settings → Import.
Import files individually; this guide does not assume a folder or archive importer.

To try it, download a file from [templates](../templates/README.md), or follow the
[project-planning example](../examples/project-planning/README.md).

## Export a page

Open the page's `…` menu and choose **Export**. Select **Markdown** for text you
want to use in another editor, or **PDF** for a document you want to share or print.
Review the export options, then choose **Export** and save the file.

The CLI can also print a note as Markdown; see the [CLI guide](cli.md).

## What to check when moving content

Markdown cannot represent every rich editor setting or layout. Page appearance,
block identities, and other app-specific details may not survive an export and
re-import. PDF is a presentation format rather than an editable vault backup.

Check attachments and links in the destination tool. Exporting a page as Markdown
does not promise to package every attachment, recreate an entire vault hierarchy,
or remap links between separately imported files. Recreate page links with `[[`
after importing related notes.

For a complete backup, copy the [whole vault](local-vaults.md#back-up-a-vault).

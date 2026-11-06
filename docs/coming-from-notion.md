# Coming from Notion

Zyler is a desktop notes app with a block editor and databases like the ones you know from
Notion. It keeps your notes in a folder on your computer instead of a workspace on a server.
This guide shows what carries over, what does not, and how to move your pages.

## What will feel familiar

- **Blocks.** Type `/` for headings, to-dos, tables, code, columns, toggles, callouts, and media.
- **Pages in pages.** Nest pages in the sidebar, and give each an icon and a cover.
- **Links.** Type `[[` to link a page. Zyler also links to a single block and draws a graph of the vault.
- **Databases.** Table, board, calendar, list, and gallery views over the same rows, with
  properties, filters, sorts, grouping, and row templates. See [databases](databases.md).
- **PDF blocks.** Show a PDF in a page and open it full screen with Space.

## What is different

- **Your notes are files.** A [vault](local-vaults.md) is a folder you choose. No account is
  needed, and notes open with no network.
- **One person, many devices.** Zyler is a personal notes app. It has no shared workspaces,
  permissions, or publishing. If your Notion is mainly a team wiki, Zyler will not
  replace it.
- **Sync is optional.** [End-to-end encrypted Sync](sync.md) keeps a vault the same on iPhone,
  iPad, Mac, Windows, and Linux.
- **No built-in AI.** Connect the assistant you already use through the [command-line tool](cli.md).

## Move your pages over

1. In Notion, open a page's `…` menu and choose **Export**. Pick **Markdown** or **HTML**, and
   choose whether to include subpages.
2. Unzip the download.
3. In Zyler, open **Settings → Import**. Choose **Text & Markdown** for `.md` files or **HTML**
   for `.html` files, pick a location, and select **Continue**. Import files one at a time.
4. Check each page, especially tables, links, and images. Recreate links between pages with `[[`.

Zyler imports Markdown, text, and HTML files. It does not import a Notion CSV, so recreate a
database in Zyler and copy its rows over. See [import and export](import-export.md) for what
Markdown can and cannot carry.

## Keep Notion until you are sure

Export first and keep your Notion workspace while you try Zyler. Back up the new vault before
you delete anything on either side.

For a longer comparison with other tools, read the
[Notion alternatives guide](https://zyler.app/alternatives/notion).

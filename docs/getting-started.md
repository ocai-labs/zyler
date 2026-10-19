# Get started with Zyler

## 1. Install the app

Download the installer for your platform from the
[latest release](https://github.com/ocai-labs/zyler/releases/latest).
See [installation](installation.md) if you need help choosing a file.

## 2. Create a vault

Open Zyler and choose **Create new vault**. Pick a folder for your notes.
If you already have a Zyler vault, choose **Open existing vault** instead.

A vault is a folder containing Zyler's note files and supporting data.
An ordinary folder full of Markdown files is not a Zyler vault; import those files
after creating a vault. You do not need to sign in to start writing local notes.

## 3. Write your first note

Create a page from the sidebar, give it a title, and start typing.
Type `/` in the editor to explore available blocks. Try a heading, a task list,
and a table. Zyler saves edits to your vault as you work.

Create another page for a related idea. Type `[[` to find and link a page in your vault.
You can use tabs and split panes to keep related notes visible together.

## 4. Import a template

1. Open the [weekly review template](../templates/weekly-review.md) on GitHub.
2. Use GitHub's **Raw** view or download control to save the file as `weekly-review.md`.
   Save the file content, rather than the GitHub HTML page.
3. In Zyler, open **Settings → Import → Text & Markdown** and choose the file.
4. Choose the import location and select **Continue**.
5. Replace the prompts with your own notes.

For a small set of connected pages, try the
[project-planning example](../examples/project-planning/README.md).

## 5. Know where your notes live

Zyler stores rich notes as `.zyler.json` files. Use Markdown import/export or the CLI
to exchange content with other tools. Back up the entire vault folder, including
its hidden `.zyler` directory. [Learn about local vaults](local-vaults.md).

Need help? Check [troubleshooting](troubleshooting.md) or [contact support](../SUPPORT.md).

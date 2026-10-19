# Troubleshooting

## Which download should I use?

See [installation](installation.md). The current macOS installer is for Apple Silicon;
Windows and Linux builds are x64. Download an installer, not a `.blockmap` or `.yml` file.

## The vault folder will not open

- Confirm you selected a Zyler vault, rather than a folder of Markdown files.
- Confirm the folder exists and your account has read/write permission.
- If the message asks for a newer Zyler version, install the latest release.
- Preserve a copy of the folder before investigating damaged files.

Do not delete hidden metadata or change format-version fields as a workaround.
Include the exact error in your support request.

## My imported note looks different

Import preserves formatting where supported, but Markdown and HTML do not map to
every editor feature. Check [import/export](import-export.md). If you saved a file
from GitHub, make sure it contains raw Markdown rather than the GitHub page's HTML.

## The `zyler` command is not found

Install it from **Settings → General → Command line tool**, then start a new terminal.
If the app reports a conflicting command or a permission error, keep that message
and [contact support](../SUPPORT.md). See the [CLI guide](cli.md).

## A note seems to be missing

Check that you opened the intended vault, search for the note, and check the app's
Trash. Preserve a backup before attempting recovery. If you have a separate vault
backup, restore it to another folder first so you can compare both copies.

## Sign-in, billing, or a connected feature fails

Local notes should remain available without sign-in. Record the app version and exact
error, then email [support@oceanai.so](mailto:support@oceanai.so). Do not post login
codes, payment information, or session tokens in a public issue.

## Still stuck?

Use [support](../SUPPORT.md) to choose a public bug report or private email. Include
your operating system, Zyler version, steps, and expected versus actual behavior.

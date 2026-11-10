# Offline edits and conflicts

## Writing offline

You can keep writing without a connection. Changes wait on the device and upload the next
time Zyler is open with a connection. Zyler syncs only while the app is open.

## When two devices change one page

Zyler merges the two versions block by block, so edits to different parts of a page both
survive. When one part was changed on both devices and cannot be merged, Zyler keeps the
newer version on the page and saves the other device's whole page in the page's version
history, labelled **Conflict copy from** and the device's name. Nothing is lost.

## Review a conflict on a computer

A notice at the top of the page reads "*Device* also changed this page, and one part didn't
merge."

1. Click **Compare**. **Version history** opens with the other device's version pinned.
2. Look through the other device's version. Copy what you need from it, or click **Restore**
   to make that version the page again.
3. When you are done, click **Release** to let the pinned version expire like other history.

Click **Dismiss** to close the notice on every device without opening the history.

## Review a conflict on iPhone or iPad

A notice reads "*Device*'s edit didn't merge." Tap **View** to read the other version.
To restore it, use Zyler on a computer.

## Other notices you may see

- **Pages disappeared outside Zyler. Uploads are paused.** Files were removed from the vault
  folder by another program. Choose **Restore cloud copies** to bring them back, or
  **Move to trash everywhere** if you meant to delete them.
- **This page was saved by a newer Zyler. Read-only here.** Update Zyler on this device to
  edit the page.

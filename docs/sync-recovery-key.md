# Your recovery key

Your notes are encrypted with keys that only your devices hold. The recovery key is the
backup of those keys: it lets a new device join when no device you already use is at hand.

## What it looks like

28 letters and digits in groups of four, like `ABCD-EFGH-JKMN-PQRS-TVWX-YZ23-4567`.
When you type it, spaces, hyphens, and letter case do not matter, and `O` is read as `0`
and `I` or `L` as `1`.

## Keep it safe

- Store it in a password manager, or on paper kept away from your devices.
- Do not keep it only inside the vault it protects.
- Zyler shows the key once, when you [turn on Sync](sync-set-up.md). It cannot show it again,
  and Zyler support cannot recover it.

## If you did not save it

Open **Settings → Sync** on a connected device. If the **Recovery key** row says **Not saved**,
click **Save key…** to finish saving it.

## Make a new key

Do this if your key may have been seen by someone else, or you lost it but still have a
connected device.

1. On a connected device, open **Settings → Sync**.
2. In the **Recovery key** row, click **Generate new…**.
3. Confirm with **Generate new key**. Your old key stops working at once.
4. Save the new key, which is shown once, just like the first one.

## If you lose the key and every device

Your synced notes cannot be read by anyone, including Zyler. Vault folders you still have on
a device, or in a [backup](local-vaults.md#back-up-a-vault), are not affected.

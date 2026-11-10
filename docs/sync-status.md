# Sync status

## Where to look

- **Settings → Sync → Status** shows the state of the open vault.
- On a page, open the **…** menu and point to **Sync** for the last sync time, **Pause sync**,
  and **Sync settings**.
- In the sidebar's vault switcher, a cloud mark shows which vaults sync.

| Status | Meaning |
| --- | --- |
| Syncing… | Changes are uploading or downloading |
| Up to date | This device has everything |
| Offline | No connection; changes wait on this device |
| Not syncing | Sync is turned off or paused for this vault |
| Download only | Your plan ended; see [plans and stopping Sync](sync-plans.md) |
| Storage full | Your plan's storage is used up |
| Connect this device to start syncing | This device has not joined yet; see [add a device](sync-add-device.md) |
| Paused | Something needs you; click **Why?** |

## When a vault is paused

Click **Why?** next to **Paused** to see the reason and the fix.

| Reason | What to do |
| --- | --- |
| Can't reach the server | Check your connection, then click **Retry**. Changes upload when you are back. |
| Storage is full | Click **Free up space**, or upgrade your plan. Changes upload once there is space. |
| Your plan ended | Click **Resubscribe ↗**. Until then the vault only downloads. |
| The cloud copy was deleted from another device | Click **Sync again**. |
| Linked to another account, or another folder already syncs it | Check that you are signed in with the account that syncs this vault, and that no other folder on this device syncs it. |
| The account removed this device | Sign in again, then connect the device as in [add a device](sync-add-device.md). |

## A vault in the cloud is not on this device

If **Settings → Sync** shows vaults in the cloud that this device has not connected to, click
**Connect…** and approve this device from a device you already use, or use your
[recovery key](sync-recovery-key.md).

## Still stuck?

Note the status text and your Zyler version (**Settings → General**), then
[contact support](../SUPPORT.md).

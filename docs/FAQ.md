# LifeDash FAQ

## Where is my data?

**Without an account**, everything stays on your Mac, in
`~/Library/Application Support/LifeDash/` or in the folder you pick with *Choose Data
Folder…*. Nothing leaves the Mac.

**With an account**, the Mac keeps its own copy and the server keeps an encrypted one,
so your data reaches your other devices. The web app keeps an encrypted copy in the
browser too, and clears it when you sign out.

You can also connect the Mac app to
your own server (*Settings › Custom*).

## What can the server see?

It **cannot** read your projects, tasks, descriptions, amounts, attachments, attachment
names or notification text. They are encrypted on your device before they leave it, with
a key the server does not have. It never receives your password either.

It **can** see what it needs to do its job:

- your username, your device names and when you signed in
- when your data changes and how large it is
- how many attachments you have and their size
- when your notifications are scheduled
- for shared projects, who is in each one, and who last changed it and when

More in [How LifeDash keeps your data safe](HOW-SECURITY-WORKS.md).

## How do I export my data?

Open **Account** in the web app, or **Settings** on the Mac, and choose **Your data ›
Download all data**. You get a zip with all your projects and tasks (`tasks.json`) and
every attachment, decrypted on your device.

## How do I delete my account?

Go to **Danger zone**, in the same place. After two confirmations, the first of which
offers to download your data, your account and your data are removed from the server for
good.

Projects you shared are handled like this: you leave the ones you joined, and each one
you created passes to the person who joined it first. If nobody else is in it, it is
deleted.

Server backups can hold an encrypted copy of the server until they
are replaced. Without your keys, that copy cannot be read.

## I forgot my password. What now?

Use the **recovery kit** you saved when you created the account. It is the only way back
in: nobody, including the server administrator, can read or recover your data without it.

If you still have a signed-in device, you can create a new kit from **Recovery kit** in
Account or Settings. The old one stops working.

## I lost my phone. Is my data gone?

No. Your data is still on the server and on your other devices. See
[the quick start](QUICKSTART.md) for how to get back in, and sign out the lost device
from your account.

## Does LifeDash track me?

No. There are no analytics or ads. On the web, the sign-up, sign-in and password recovery
pages use Cloudflare Turnstile to stop bots, so Cloudflare handles those requests.

## Who can see a shared project?

Only the people in it. What is shared and what stays yours is explained in the
[README](../README.md#share-a-project). The € fields on the project and its tasks are
shared. Amount, invoice and payments are not.

## Can I use it from scripts or AI agents?

Yes, with the `lifedash` command. See the [command reference](CLI.md).

# LifeDash quick start

Five minutes from download to your tasks on the phone.

## 1. First launch

1. Download **[LifeDash.zip](https://github.com/antarcorrado/lifedash/releases/latest/download/LifeDash.zip)**,
   open it and drag **LifeDash** to Applications. It needs macOS 13 or later.
2. Open it. The first time, the **Settings** window explains what an account is
   for. You can close it with **Not now**: LifeDash works on the Mac without an
   account, with your data in one file on this Mac.
3. Press **+** to create a project, then add tasks to it.

By default LifeDash lives in the menu bar (click its icon to show the window). To
put it back in the Dock: *View › Menu Bar Mode*.

## 2. Create an account

An account gives you the same projects and tasks on the phone and on the web,
always in sync, plus due-date notifications even when the Mac is off. Everything
is encrypted on your device before it leaves: the server cannot read it.

On the Mac: **LifeDash › Settings…** (⌘,), then **Create an account**. Or in any
browser at [antarcorrado.com/lifedash](https://www.antarcorrado.com/lifedash/).

1. Choose a **username** and a **password** of at least 12 characters. The
   password never leaves your device and cannot be reset by anyone: use a
   password manager.
2. **Scan the QR code** with an authenticator app (Apple Passwords, Google
   Authenticator, 1Password, Authy…) and type the 6-digit code it shows. From now
   on every new device asks for a code. Not ready? **Later** gives you 14 days.
3. **Save the recovery kit** (next section). The app shows it only once.

A Mac that is already in use joins the account with its tasks: the first sync
merges what is on the Mac with what is on the server.

## 3. Connect your phone

1. On the phone, open **[antarcorrado.com/lifedash](https://www.antarcorrado.com/lifedash/)**
   in Safari (or any browser) and sign in with username, password and code.
2. Add it to the Home Screen: in Safari **Share › Add to Home Screen**. It then
   opens like an app and works offline.
3. For due-date notifications, allow them when the app asks (on iPhone this needs
   iOS 16.4 or later and the app on the Home Screen).

Changes made on the Mac reach the phone within seconds, and the other way round.

## 4. The recovery kit

At the end of sign-up you get a **recovery kit**: a text file to download, copy or
print. It contains:

- a **recovery key** (32 characters): it opens your data if you **forget your
  password**;
- eight **emergency codes**: each one replaces the 6-digit code once, if you
  **lose the phone** with the authenticator app.

Keep it somewhere safe and **away from that phone**: a password manager, a printout
in a drawer, an encrypted drive.

### What happens if you lose something

| You lost | What you can do |
| --- | --- |
| The password | On the web: **Forgot your password?**, then the recovery key and a code (or an emergency code). You choose a new password; every device signs in again. |
| The phone with the authenticator app | Sign in with an **emergency code** instead of the 6-digit one. Each code works once; the account panel shows how many are left. |
| The recovery kit, but you still know the password | Nothing changes day to day. But you no longer have a way back if you forget the password, so keep it in a password manager, and download your data now and then (**Your data › Download all data**). |
| Password **and** recovery kit | Your data cannot be opened any more, by anyone, not even the server administrator. This is the price of end-to-end encryption. A Mac that is still linked keeps working: from its Settings, **Download all data** saves a copy of everything. |

## Next steps

- [README](../README.md): everything LifeDash does, Finance, the `lifedash` command
  and AI agents.
- [CHANGELOG](../CHANGELOG.md): what changed in each version.
- Problems or ideas: [open an issue](https://github.com/antarcorrado/lifedash/issues).

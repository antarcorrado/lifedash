# How LifeDash keeps your data safe

This page explains it without the technical terms. To report a security problem, see
[SECURITY.md](../SECURITY.md).

## The short version

Your projects and tasks are locked on your device before they travel, and only you have
the key. The server stores the locked copy so your devices stay in sync, but it cannot
open it. Neither can whoever runs the server.

## What stays private

- Projects, tasks, descriptions and amounts
- Attachments and their names
- The text of your notifications
- Your password, which never reaches the server

## What the server does know

A postal service can't read a sealed letter, but it knows when one was sent and how heavy
it is. In the same way, the server knows:

- your username, your device names and when you signed in
- when your data changes, and how large it is
- when notifications are scheduled
- for shared projects, who is in each one and who changed it last

The administrator of the official server can see the list of usernames, their status and
when they joined, and a log of account events such as sign-ins. Never your content.

## How your account is protected

- **A password and a code.** Each new device needs your password and a code from an
  authenticator app. New accounts have 14 days to add the code.
- **Passkeys.** On the web you can sign in with Face ID, Touch ID or your device PIN.
- **Limits on guessing.** Repeated wrong attempts are slowed down and temporarily blocked.
- **Recovery kit.** It is your way back in if you forget your password, and it is shown
  only once. Keep it somewhere safe.

## Shared projects

Each shared project has its own key, which opens that project and nothing else in your
account. When someone leaves, the project gets a new key and they stop seeing changes,
although anything they already saw or downloaded stays with them. Shared projects are
never public pages.

To be sure you are sharing with the right person, compare your key fingerprints out loud.
You will find them in the project's Share section.

## What LifeDash can't protect you from

No system is perfect, so these limits are worth knowing:

- **A weak password.** If someone stole the server's files, they could try to guess it.
  Use a long, unique one.
- **The web app comes from the server.** If someone took control of the server, they could
  change the page to capture your password as you type it. The Mac app doesn't have this
  problem, because its code is already on your Mac.
- **Shared keys pass through the server.** A compromised server could hand out a false
  key. That's what the fingerprint comparison is for.
- **Tokens for scripts and agents.** A token opens your data without your password. Revoke
  the ones you no longer use.
- **Your own devices.** Anyone who can unlock your phone or Mac can open what is on it.
- **A lost recovery kit.** If you lose your password and your kit, nobody can recover your
  data. That is the price of nobody else having your key.

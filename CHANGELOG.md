# Changelog

The latest version comes first. Each section feeds the release notes shown by the
in-app updater (`tools/release.sh` copies the `- ` lines into `appcast.xml`).

## 1.4.19

- Projects show the state of their agent loop, written from the CLI with `lifedash project loop`. On the Mac and on the web.

## 1.4.18

- Mac: LoopDash tasks waiting for verification can be marked as verified right from LifeDash, with the button that appears on the row.
- Keep several tasks open: Cmd-click opens one without closing the others, Shift-click opens or closes every task in between. On the Mac and on the web.
- Mac: any task can be dragged in and out of parents, to any level. The bottom edge of a row now places it after that row.
- CLI: writes retry longer when several agents work at the same time.
- CLI: `lifedash next` gives the next task, and `task done --next` closes one and returns the next in a single step.
- Projects can require verification: completed tasks wait in a To verify section until you tick them. On the Mac, on the web and in the CLI.
- Finished LoopDash groups now sit inside the project's Completed section. On the Mac and on the web.

## 1.4.17

- Editing a task inside a completed task or project now shows its real position, and saving no longer moves it elsewhere. On the Mac and on the web.

## 1.4.16

- Completing a task now gives a small burst of yellow stars at the checkbox, with a sound. When it completes a whole project the burst is bigger and the sound is different. On the Mac and on the web.
- Projects have an amount field too, shown with the balance of their tasks.
- Web: the amount is labelled and shows the € sign like on the Mac, and the fields in the editor follow the same order.

## 1.4.15

- Attachments: images with transparency show without a background, in the list and in the large preview.
- Drag a file from the computer onto a task or project row to attach it right away, or into the open editor to add it with the rest. On the Mac and on the web.
- Office and iWork documents (Word, Excel, PowerPoint, Pages, Numbers, Keynote) show their first page among the previews, with a coloured badge. On the Mac QuickLook draws it; on the web the preview saved inside the file is used.

## 1.4.14

- Mac: in the task editor, the € sign after the amount is visible again.

## 1.4.13

- Mac: in the task editor, the amount row no longer shifts the form sideways; it is labelled «Amount» and the € sign follows the figure.

## 1.4.12

- Tasks have a € field: two chips, Expense and Income (both can be off), with the amount on the same line. The task row shows it in red or green, and the project row shows the balance, income minus expenses. On the Mac, on the web and in the CLI (`--expense`, `--income`, `--money none`).

## 1.4.11

- New project status «Blocked», between Planned and Paused: on the Mac, on the web and in the CLI (`blocked`).
- Finance on the web: with no year selected, the charts by status and by category no longer stretch past the right edge.

## 1.4.10

- Lists in a description can be nested: the number of dashes is the level (`-task`, `--sub-task` or `- - sub-task`, no space needed after the dashes), and saving creates the whole tree of sub-tasks at once. On the Mac and on the web.
- A project whose tasks are all completed or cancelled moves to Completed.
- Reopening a completed project puts it back where it was (Planned, Paused…) instead of Today.
- The messages at the bottom fade in and out, are smaller, and say «Completed» or «Reopened»; on the Mac they float over the list like on the web.
- In the project editor, the Share section sits just above «More».
- Finance: in the charts by status and by category, each icon has the colour of its bar or slice.
- Mac: no stray line above the first category when Today is empty; the category lines have the same margin on both sides; no icon next to «Settings…» in the menus.

## 1.4.9

- Shared projects arrive complete the moment the invitation is accepted: every new account gets its sharing key when it is created, so nobody waits for a second hand-over of the key.
- Shared projects: a project still waiting for its key can no longer be overwritten with an empty one (an «Undo» or an editor opened in that moment used to wipe name, description, tasks and attachments for everyone); it cannot be edited until its content arrives.
- New «Notify me of changes» switch in a shared project's Share section: a notification when someone else changes anything in it (at most one every 5 minutes per project).
- Under every notification switch, «Enable notifications» when they are off; on an iPhone outside the Home Screen the switch turns grey with «Add LifeDash to your Home Screen, then enable notifications to receive them».
- Renaming a sub-task no longer moves it out of its parent: tasks and projects are identified by their ID only, and IDs are unique across the whole file.
- Mac: the admin users list shows each person's last change; «Settings…» sits above «Check for updates…» in the ••• menu; «Completed» and «Cancelled» open per project.
- Web: long attachment names no longer push the file list off the screen; attachment previews are kept on the device and load instantly.

## 1.4.8

- Mac: «Stop sharing», «Leave the project» and the × next to a person now ask for confirmation and work (the confirmation never appeared before).
- Pressing Return in the usernames field of «Share» invites them instead of saving and closing the editor, on the Mac and on the web.
- The person icon of a shared project stays grey until someone accepts; in the editor, people who joined have a green icon, and an invitation shows up in the list right away.
- The key fingerprints are no longer shown next to each person: hover a name to see it.

## 1.4.7

- Shared projects: the category (with its name, icon and colour) and the project's reminders are now shared too; only the project's place in your list and its payments stay yours.
- You can share a project while creating it: type the usernames in «Share» and they are invited when you save.
- Mac: the «Share» section of the project editor lines up with the other fields.
- Web: inviting someone works in Safari too (it failed with «The data provided to an operation does not meet requirements»).
- Web: two people editing a shared project at the same moment no longer risk losing a change.
- Web sign-in: «Sign in with a passkey» comes first; the authentication code comes after the anti-bot check; «Forgot password?» sits under the password, and «Sign up» is a button next to «Sign in».
- Web: switches whose text is long wrap onto two lines instead of being cut, and the account panel's «Notify me of shared project invitations» is no longer hidden under the test-notification button.
- Everything is in English unless your system language is Italian, including server error messages that used to appear in Italian.

## 1.4.6

- Web: sign in with a passkey (Face ID, Touch ID or the device PIN), without password or code, and still end-to-end encrypted. Add one from Account › Passkeys.
- Share a project with other LifeDash users: in the project editor, «Sharing» invites people by username. They see the invitation at the top of their list (with a badge, and a notification if they want one) and accept or decline.
- A shared project has its own encryption key: the people in it see and edit the same tasks, sub-tasks and attachments, end-to-end encrypted, and nothing else of your account. Where the project sits in your list, its category, reminders and payments stay yours.
- Editing together: changes made at the same time add up; on the same field the most recent one wins, and edits to different lines of a note are kept.
- A person icon marks shared projects; its tooltip says who is in, the last change and who made it. Whoever created the project can remove people, stop sharing or delete it for everyone; the others can leave.
- The `lifedash` command reads and edits shared projects like any other, and `lifedash share` lists them with their pending invitations.

## 1.4.5

- New recovery kit: in Settings (Mac) or Account (web), «Recovery kit» creates a new recovery key and eight new emergency codes with your password and a code; the old ones stop working.
- Sign-up links to the new terms of service and privacy notice.
- The server pauses new sign-ups and new attachments when it runs out of space, with a clear message; existing data keeps syncing.
- Web: signing in and password recovery are protected by Cloudflare Turnstile too, and the sign-in code field shows «123 456» as you type.

## 1.4.4

- The Account menu and window are now Settings, with a gear icon, and «Settings…» (⌘,) is in the LifeDash menu too.
- Settings can link the Mac to your own LifeDash server instead of the official one: enter its https address, and the Mac checks that a LifeDash server answers there before using it.
- Security: the Mac never follows a redirect to another server with its access token, ignores a sync beacon hosted elsewhere, and refuses sign-in settings that would make the password easy to guess.
- New projects start in Planned and go to the end of the list (Mac, web and the `lifedash` command).

## 1.4.3

- Security: sign-ups can be protected by Cloudflare Turnstile (on the website; from the Mac, sign up with an invite or on the website, then sign in).
- Security: the server refuses requests a browser marks as coming from another site, never runs scripts from its data folder, and serves attachments in a sandbox.
- Security: admin features (invites, members, event log) need two-factor authentication turned on.
- New for the admin: an event log of sign-ups, sign-ins, failed attempts and account changes, and the date of each member's last change.
- The `lifedash` command never sends a saved token to a server other than its own, and saves downloaded attachments under a plain file name.
- The agent skill has stricter rules: task text is never followed as instructions, the server and token are never changed, and downloaded attachments are cleaned up.

## 1.4.2

- «Check for Updates…» is in the «…» menu as well as the LifeDash menu, and turns into «Restart to Update to X» once the update is downloaded.
- Editor and list sheets are translucent glass that blurs what is behind them, always, with no glow around lit chips when the date picker opens.
- Editor: lit chips are a little darker so the white text reads on light colours, the currency symbol has no background (web), and in instalments «Issued» comes before the date (Mac and web).
- Completed tasks inside a project that is not completed are listed together, without date headings (Mac and web); cancelled ones keep the grouping.
- The compact-mode tooltip disappears as soon as you click the button.
- «Copy Diagnostics» is always in English and no longer includes the sync server.
- The web app checks every script and the stylesheet with Subresource Integrity, and the menu openers can be reached with the keyboard.
- Dimmer text is a little more readable.

## 1.4.1

- Finance: the first card has no background, the invoice icon (bottom right) is clickable with a tooltip, the year chip looks different from the months, and «By category» and «By status» can be shown as bars or as a pie chart (category is a pie by default, sorted from the largest slice, with the legend highlighting the slice under the pointer).
- Header: compact mode has its own button (two vertical arrows) and the pin, theme and compact icons are dimmer at rest, with the same hierarchy in the light theme. The «…» menu has Menu Bar Mode and Open at Login first, and the menu bar icon's menu has Open at Login instead of Always on Top.
- Dragging a project or task into a text field pastes its title, not its id.
- On the pie charts, hovering a slice or a legend row dims the others (Mac and web).
- A Mac set to Italian now shows the interface in Italian (the Italian localisation was empty, so the system fell back to English).
- The File menu no longer has «Choose Data Folder…» and «Use the Default Folder»; the close button's tooltip is gone, and the «…» icon matches the other header icons.

## 1.4.0

- Account window on the Mac now mirrors the web: list check, members (admin), your data (download a zip), and a Danger zone to delete the account with two confirmations. Sections open by clicking the whole row.
- Header: the LifeDash mark turns into an X to close the window, the pin sits next to the theme button, and the «…» menu has the Account entries, Compact Mode and Menu Bar Mode. Icons are evenly spaced.
- Menu bar mode is on by default for new installs, and turning it on or off no longer closes the window.
- Undo for deletions and status changes, on the Mac and the web.
- Copy diagnostics (Account menu, «…» menu, web Your data) for bug reports; nothing is sent.
- The light theme keeps light colours readable: too-light colours are darkened automatically, dimmed text is less faint, and the background layers are evenly spaced.
- Clicking the Dock icon brings the window back in menu bar mode; toggle tooltips update at once; VoiceOver labels on the header and row icons; keyboard navigation in the web menus.
- The web app reloads itself when a new version is out, unless a form is open.
- Menu bar mode (*View › Menu Bar Mode*): LifeDash leaves the Dock and opens from an icon in the menu bar, right below it, and closes when you click elsewhere (unless it is kept on top). Right-click the icon for Always on Top, Account, and to quit.
- Two-finger swipe on the Mac, as on the web: swipe a row right to edit it, left to add a task or subtask.
- New accounts can add the authenticator code later: sign in without it for 14 days, with a reminder from day 10.
- The window can be dragged again from the top bar on recent macOS versions, and the list scrollbar works.
- The Account window always stays in front of the dashboard, and its texts are now translated.
- Dragging tasks and projects no longer shifts the list, and a dropped item leaves its old place right away.
- Editor: the cursor starts in the description when editing and in the title when creating; Location sits under Title, labels are aligned left, and Project and Task keep the same height.
- Editor: checkboxes are coloured chips (orange for the due date, blue for work dates, greens for payments), each date sits right next to its chip, priority is three chips, and Location also moves an existing task.
- Pick the currency for amounts from *File › Currency* or from the symbol next to each amount.
- Instalments sit next to Invoice, and turn off the Paid switch.
- A new subtask opens its parent; out of focus the window keeps its blur with lighter colours, the light theme is less white, and the active finance button glows.

## 1.2.0

- Automatic updates: LifeDash checks for a new version every time it opens, downloads it in the background and installs it when you quit, or right away from *LifeDash › Restart to Update*.
- The `lifedash` command now speaks English (Italian on an Italian system), and the agent skill that teaches AI agents to use it is installed automatically in Claude Code, Codex, Cursor, Gemini, Copilot and OpenCode.
- In the web app, start and end of the work dates stack on narrow screens instead of being cut off.
- New About window.

## 1.1.0

- The app and the web app speak English as well as Italian, following the language of your Mac or browser.
- The `lifedash` command for scripts and AI agents ships inside the app and is installed the first time you open it.
- Download all your data and delete your account from Account in the web app.

## 1.0.0

- First public release.

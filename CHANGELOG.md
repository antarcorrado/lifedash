# Changelog

The latest version comes first. Each section feeds the release notes shown by the
in-app updater (`tools/release.sh` copies the `- ` lines into `appcast.xml`).

## 1.4.45

- The year chart in Finances shows the monthly average as a dashed line, with its amount written next to the total.
- Months without income have a grey point on the year chart.
- Each point on the year chart shows its own amount on hover.

## 1.4.44

- The year chart in Finances shows every month between the first and last income, including quiet ones.
- Hovering a point on the year chart enlarges it and shows the amount instantly.

## 1.4.43

- Opening a category, a project or a task shows what's inside neatly collapsed.
- In Finances, choosing a year shows a dot-and-line chart of the money collected month by month.

## 1.4.42

- Search on the Mac stays smooth even with a single letter: the list filters right away, and rows open with their details from two letters on.

## 1.4.41

- Start typing a letter or a number anywhere in the list and the search opens with it.
- When a search finds nothing, a «Create project» button opens a new project already named after the search.
- The project editor points out when another project already has the same title, with a link to open it.
- Search on the Mac is much quicker on long lists.
- Claude Desktop can now use LifeDash in chat mode too: the app sets it up automatically.
- A newly enabled agent loop starts in single-agent mode.

## 1.4.40

- Search waits for a one-second pause in typing, so it stays smooth on long lists, and only the tasks that contain the searched words open up.
- Long descriptions end with «… Expand», and the «More…» button has its dots too.
- Completed and cancelled tasks, including completed subtasks, sit behind «Completed…» and «Cancelled…» buttons in the same style as «More…», aligned with the other rows.
- The loop icon shows one dot for single-agent and three dots in a triangle for subagents.

## 1.4.39

- Tasks to verify use their own seal-with-tick icon, in the «To verify» section, on its «verify all» button and on each row, so they no longer look like completed tasks.
- Task rows are cleaner: no question mark appears when the state of a commit cannot be read.

## 1.4.38

- Tasks waiting for verification, and the «verify all» button of their section, now show a clear tick.

## 1.4.37

- Opening LifeDash from the menu bar is now instant: the window appears right away and refreshes its data only if something changed.
- The first click on the window counts even when another app is in front: buttons, rows, fields and dragging the window all respond at once.
- Search is lighter: the list filters after a brief pause in typing, and the search field sits on a blurred background that stays readable over the list.
- A task whose open sub-tasks are all blocked now shows as blocked too, and goes back to normal as soon as one is unblocked.
- The «To verify» section has a tick to verify all its tasks at once, on the Mac and on the web.

## 1.4.36

- «Restart to update» now does what it says: the app closes, the new version installs and LifeDash opens again by itself.
- Settings are easier to read: the title reads «Settings» with your username in grey beside it, entries are grouped into sections with icons, and the window keeps a fixed height with scrolling, so opening a section no longer moves anything.
- The «…» menu shows the app version in grey, with «Check for updates» and «Settings» right below it.
- On the web, Settings gets the same sections and icons, and a cleaner gear icon.

## 1.4.35

- The update window now appears in front of the app even when it is set to stay always on top, so a new version can no longer hide behind it.
- The buttons at the top right of the list sit on pure blur, with no tint: on a plain background nothing shows, and the blur appears only when text scrolls underneath.
- In Settings, opening or closing a section no longer makes the content above jump and settle back.
- On the web, the text under «Download all data» in Settings is fully readable.

## 1.4.34

- Updates are checked every time you open the app (if the last check was more than an hour ago) and then every hour, so a new version is found and downloaded in the background without opening the menu.
- On the web, the settings button is now a gear and the test-notification button sits on the left.

## 1.4.33

- The end-of-loop notification on the web now names the project on every device, including a phone that unlocks with Face ID: the name stays encrypted and only your own browser can open it.
- Search is easier to read: while you search, every category opens (completed ones included) and closes again as it was afterwards, and an empty search says «No results».
- Empty project categories stay out of the way, and appear only while you drag a project.
- Web search opens reliably when you tap the magnifying glass.

## 1.4.32

- Automatic updates now complete on their own: the new version is downloaded in the background and installed when you quit, so the next launch opens the updated app. «Restart to update» stays in the menu for those who want it right away.

## 1.4.31

- The web notification at the end of the agent loop can now name the project («The loop of LifeDash has finished»). The name travels encrypted and only your own browser can open it.

## 1.4.30

- Attachment thumbnails can be copied and dragged out: right-click gives «Copy image» (or «Copy file»), and dragging a thumbnail drops the file into Finder and other apps such as Claude.
- Thumbnails keep the original proportions of the image, up to 21:9 wide or 9:21 tall, so the whole picture is easier to see.
- The search field closes with a click outside when it is empty, blends into the page background, and highlights the searched words in titles and descriptions.
- The icons at the top right of the list sit on a soft blur instead of a solid background, and the expand buttons are always available.
- The task row stays cleaner: the last-modified date no longer appears on hover.

## 1.4.29

- Instant search in the list: the magnifying glass next to the other icons opens a field that filters projects and tasks as you type (titles, descriptions, notes and attachment names), with a small X to clear it.
- The icons at the top right of the list now float in place like the + button while the list scrolls.
- Task and project titles show their tooltip only when they are cut off.

## 1.4.28

- The deploy mode chip «Solo locale» is now simply «Locale», and the project editor widens to fit its longest row of chips.
- The app now also installs the agent loop's slash commands (`/fix`, `/feature`, `/run-agent`…) and keeps them up to date with every update.
- In folders linked to a LifeDash project, agents track every piece of work as a LifeDash task on their own, keeping its status current.
- The `lifedash` skill is clearer and more consistent: each command points to one place in the guide.

## 1.4.27

- The status chip is always visible on every open task, not only under the pointer.
- «More» is now a button: pressing it shows the other tasks at the same level as the rest of the list, and it comes back when the project is collapsed again.

## 1.4.26

- The agent loop's FTP mode is now called Publish online, and also covers projects with their own deploy; existing projects keep working as they are.
- The deploy and execution tooltips are narrower and clearer, and the chips are in a new order.
- A task's icon always takes the colour of its status, like the status chip.
- On the web, PowerPoint, Word and Excel files without an embedded image get a drawn preview, and passkey sign-in tells the Face ID unlock key apart.

## 1.4.25

- The project editor can pick the agent loop's FTP site from a menu, and add or edit sites right there; site profiles stay on this Mac and never reach the server.
- New `lifedash site` and `lifedash tools` commands manage the site profiles and the programs the deploy uses on this computer.
- The agent loop status uses the loop arrows, and the deploy and execution tooltips appear instantly.

## 1.4.24

- The agent loop status is a menu in the project editor, and the deploy and execution modes explain themselves in a tooltip.
- Every project with an agent loop shows its arrows in the list, coloured by the loop status.
- On the web the agent loop fields sit one below the other.
- The `lifedash` skill now covers FTP deploy and ZIP export of the agent loop on its own, configured per project.

## 1.4.23

- The Agent loop section of the project editor lines up with the other fields, with labels on the left.
- The project list marks agent loops with their arrows, next to the status.

## 1.4.22

- The project editor has a Loop chip: status, deploy mode, execution mode and current task of the agent loop, with icons. On the Mac and on the web.
- In the project list the loop status shows with its icon, only while the loop is doing something.
- The `lifedash` skill now includes the whole agent loop: setup, commands and protocol in one place.

## 1.4.21

- Skill: each project now links to LifeDash through a small project file.

## 1.4.20

- Agent loops, verification and queues now all live in your projects.

## 1.4.19

- Agents can send a notification when their loop stops. The project name never reaches the server.
- Projects show the state of their agent loop, written from the CLI with `lifedash project loop`. On the Mac and on the web.

## 1.4.18

- Keep several tasks open: Cmd-click opens one without closing the others, Shift-click opens or closes every task in between. On the Mac and on the web.
- Mac: any task can be dragged in and out of parents, to any level. The bottom edge of a row now places it after that row.
- CLI: writes retry longer when several agents work at the same time.
- CLI: `lifedash next` gives the next task, and `task done --next` closes one and returns the next in a single step.
- Projects can require verification: completed tasks wait in a To verify section until you tick them. On the Mac, on the web and in the CLI.

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

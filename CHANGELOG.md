# Changelog

The latest version comes first. Each section feeds the release notes shown by the
in-app updater (`tools/release.sh` copies the `- ` lines into `appcast.xml`).

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

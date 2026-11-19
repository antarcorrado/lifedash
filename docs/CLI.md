# The `lifedash` command

Read and change your projects and tasks from the Terminal, a script or an AI agent. The
command ships inside the Mac app and needs [Node.js](https://nodejs.org) 18 or later.
Messages are in English, or in Italian on an Italian system.

## Setup

```bash
lifedash --help
```

If the Terminal answers *command not found*, add the folder the app linked it into to
your `PATH` (`/opt/homebrew/bin`, `/usr/local/bin` or `~/.local/bin`), or call
`/Applications/LifeDash.app/Contents/Resources/cli/lifedash.mjs`.

Create a token in the web app (**Account › Tokens for scripts and agents**) or on the Mac
(**Settings › Tokens for scripts and agents › New token…**). Choose *read only* if the
agent should only look. Then:

```bash
lifedash login        # paste the token and press Enter
lifedash whoami       # checks that it works
```

The token is saved in `~/.config/lifedash/credentials.json`, readable only by you.
Instead of the file you can set `LIFEDASH_TOKEN` and `LIFEDASH_SERVER`. It is never
passed as an argument.

**A token opens your data without your password or code**, so treat it like a password.
You can revoke it from the same panel. `lifedash logout --revoke` also revokes it on the
server.

## Reading

| Command | What it does |
|---|---|
| `lifedash projects` | projects, without the completed ones unless you add `--all` |
| `lifedash project <id>` | a project with its task tree |
| `lifedash tasks` | tasks, sub-tasks included |
| `lifedash task <id>` | a task with description and sub-tasks |
| `lifedash types`, `lifedash categories` | your task types and project categories |
| `lifedash doc` | the whole document, as JSON |

**Filters for projects:** `--status`, `--all`, `--category`, `--paid yes|no`, `--search`.

**Filters for tasks:** `--project`, `--parent`, `--status`, `--open`, `--leaves`, `--type`,
`--priority`, `--search`, `--due-before`, `--overdue`.

**On both lists:** `--sort due|created|started|completed|priority|title`, `--reverse`,
`--first N`, `--last N`, `--count`, `--ids`.

## Tasks

A token that can write is needed here and in the next sections.

```bash
lifedash task add --project ID --title "Header" [fields]
lifedash task add --project ID --titles -              # one task for each line of stdin
lifedash task set <id>… [fields]
lifedash task start|done|pending|block|cancel <id>…    # with optional --note, --commit
lifedash task move <id>… --under TASK | --to PROJECT | --before TASK | --last
lifedash task dup <id>
lifedash task rm <id>…
```

Fields: `--title`, `--desc`, `--type`, `--priority`, `--status`, `--due`,
`--expense AMOUNT`, `--income AMOUNT`, `--money none`, `--notify MINUTES[,MINUTES…]`,
`--note`, `--commit`, `--retries`, `--created`, `--started`, `--completed`, and `--parent`
or `--id` when adding. `--new-id` changes an id.

## Projects

```bash
lifedash project add --name "New site" [fields]        # starts in Planned
lifedash project set <id> [fields]
lifedash project move <id> --before PROJECT | --last
lifedash project dup <id>
lifedash project rm <id>
```

Fields: `--name`, `--desc`, `--category`, `--status`, `--due`, `--notify`,
`--created`, `--started`, `--completed`, `--work-start`, `--work-end`, `--expense`,
`--income`, `--money none`, `--paid yes|no`, `--amount`, `--invoice yes|no`,
`--invoice-issued yes|no`, `--payment-expected`, `--payment-date`, `--paid-amount`, and
`--payment-parts N[@DAY][@issued][,…]`.

`none` removes an optional field.

## Attachments

```bash
lifedash task files <id>
lifedash task attach <id> <path>…
lifedash task detach <id> <file-id|name>…
lifedash file get <file-id> [--out PATH] [--force]     # saved decrypted
lifedash file rethumb [--force] [--dry-run]
```

The same works with `project` in place of `task`. Each file can be up to 10 MB, with up
to 20 per item.

## Shared projects

```bash
lifedash share            # shared projects: with whom, last change and author
lifedash share invites    # invitations waiting for an answer
```

Tasks in a shared project are read and changed like any other, and the change reaches
everyone with your username as the author. Inviting, accepting and leaving happen in the
app.

## Writing safely

- Several ids in one command are a single write: they all change, or none does.
- `-` in place of the ids reads them from stdin.
- `--dry-run` shows the result of any write without saving it.

```bash
lifedash tasks --project site --status pending --first 5 --ids | lifedash task start -
lifedash task rm task-1a2b3c4d task-5e6f7a8b --dry-run
```

## Output and exit codes

Output is compact by default. `--json` gives JSON, and `--full` gives every field.

| Code | Meaning |
|---|---|
| 0 | success |
| 1 | error |
| 2 | wrong usage |
| 3 | not found |
| 4 | access denied |

### Loop state

```bash
lifedash project loop <id> --status running --deploy publish --exec subagents --task <task-id>
```

Stored on the project and shown on its row. Every write refreshes the time: a running loop
silent for 30 minutes shows as no signal.

### Task chains

```bash
lifedash next --project <id> --start                 # next task, marked in progress
lifedash task done <id> --commit <hash> --next --start   # close it and get the next one, in one write
```

`next` picks open leaf tasks and skips blocked ones: the task already in progress first, then
urgent, then project order, low priority last. `--parent <task>` limits it to one parent.
The answer has `next` and `remaining`; `next` is null and the exit code is 3 when nothing is
left. `--next` also works with `block` and `cancel`.

Changes reach the Mac and the web at their next sync.

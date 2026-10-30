# Where Claude Desktop schedules live, and whether to move them to Claude Code

Notes from checking whether Claude Desktop schedules could be migrated to Claude Code.

## Where to look

- **Local Desktop tasks:** the scheduled-tasks tool lists them, backed by `scheduled-tasks.json` files under the app's data folder (one each for Cowork and Code). Empty lists mean nothing is stored locally.
- **Cloud routines:** schedules created on claude.ai are cloud routines tied to your account. Claude Code's `/schedule` uses the same system, so they are already in Claude Code and there is nothing to move.
- Schedules are per account and per machine. If you cannot find one, check a different account or organisation, or the computer it was created on.

## Should a routine move to the cloud?

Only if it does not need your Mac. Check each one:

| Needs the Mac? | Example | Why |
|---|---|---|
| Yes | Sorting or renaming chats | Works through a browser on the Mac that is signed in to claude.ai; a cloud run has no such browser |
| Partly | Refreshing Word checklists stored in SharePoint | Connectors can read files but cannot hand over the `.docx`; editing and screenshots need the local browser |
| No | Email, Slack and calendar briefs | Pure connector work, runs fine in the cloud |

Local routines are missed if the Mac is asleep or offline at run time. Keep it awake and online, and keep the browser signed in.

## Housekeeping checklist

- Upgrade routines pinned to older models where sensible.
- Look for routines that are switched off by mistake.
- Routines that ask for input every run are templates, not timed jobs.

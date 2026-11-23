# AI Workbench Starter

[中文](README.md) ｜ **English**

Too many AI windows open, and who is doing what lives only in your head?

This is a skill for your AI to read. It sets up five things in one folder on your computer, so any window or any AI can pick up where the last one stopped:

| Five things | What they fix |
| --- | --- |
| Inbox | Your AI keeps asking you. Only two kinds get through: things you must do, things you must decide |
| Task sheets | Pasting the same text into window after window. One sheet per task, with what done looks like |
| Checks | "Done!" when it isn't. A new window looks at the evidence; no evidence means not done |
| Night shift | Work stops when you sleep. It moves what it can and puts the rest in the inbox |
| Handoff | Long chats forget. One page per job; whoever takes over reads it first |

Each morning you read one page: `home.md`.

## What you need

An AI that can read and write files on your computer. A web chat alone won't do. Everything is plain text. Nothing to install, no network.

## How to use it

1. **Code → Download ZIP**, then unzip.
2. Tell your AI (use your own path):
   > Read `ai-workbench-starter-en/SKILL.md` and follow it. Set up a workbench for me.
3. Assign something:
   > Assign: sort the files in my downloads folder by type. Make a list first, don't move anything.
4. In a new window:
   > Read `ai-workbench/rules.md` and `ai-workbench-starter-en/SKILL.md`, then check that task.
5. Next day:
   > Morning page.

If your client has a skills folder, you can put `ai-workbench-starter-en` there (not yet tried client by client).

## What has been tested

On 2026-11-23 the English version was run through the Gemini command line with sample files: set up, assign, tentative-delete question, night shift, morning page, and a check in a new window. It stopped instead of deleting, and stopped before sending an email. Each step was run once. The Chinese version was also run in Doubao Work and WorkBuddy. Other AIs that can read and write local files should work, but have not been tried.

## What it does not do

- It does not start by itself. You say the word, or use your client's scheduler.
- It does not push messages into other windows. A task counts as received once the new window reads the file.
- Spending, sending, deleting and logins always stop and wait for you. These are instructions to the AI, not a system-level lock. Back up anything important first.

## License

[MIT](LICENSE). Use it, change it.

---
name: ai-workbench-starter-en
description: Set up a personal AI workbench in a local folder and work by it - inbox, task sheets, acceptance checks, night shift, handoff, and one page to read each morning. Use when the user says "set up a workbench", "get my AI windows under control", "assign this task", "check whether this is really done", "keep working tonight", "take over this job", or "show me the morning page". Works with any AI that can read and write local files. Installs nothing, uses no network.
---

# AI Workbench Starter

The problem: with many AI windows open, who is doing what, and how far along, lives only in your head. The fix: put it all in one folder. Any window, any AI, reads the files first and then works.

## Rules that always apply

1. **Spending money, sending anything to other people, deleting or overwriting originals, logins and passwords**: always stop and put it in the inbox. Unless the user has clearly approved this specific item, it is not approved.
2. **If you cannot verify it, write "unverified".** Never make up progress, numbers or results.
3. **The AI that did the work cannot declare it done.** It may only write "awaiting check". It is done after a new window has checked the evidence.
4. **Only touch the workbench folder and the folders named in the task sheet.** Never overwrite an existing file; if the name is taken, stop and ask.
5. Never write passwords, keys, ID or card numbers, or customers' private data into the files.

## Which step does the user want?

| The user says | Do |
| --- | --- |
| set up a workbench, get my windows under control | 1. Set up |
| assign a task, do this and keep track of it | 2. Assign |
| check it, is it really done | 3. Check |
| keep going tonight, I'm going to bed | 4. Night shift |
| take over, where did we leave off | 5. Handoff |
| morning page, what needs me today | 6. Morning page |

Except for "Set up", start every session by reading `rules.md`, `inbox.md` and that job's `handoff/<job>.md`. If there is no `rules.md`, the workbench does not exist yet: do step 1 first.

## 1. Set up

1. Ask these three questions together. If the user says "you decide", use the default in brackets:
   - Which folder should it live in? (create `ai-workbench` in the current folder)
   - What are you working on? One line each, five at most. (just one sample job, "Tidy the downloads folder")
   - Besides rule 1 above, what else needs your approval? (nothing)
2. Create this, copying from `templates/` and filling it in:
   ```
   ai-workbench/
     home.md           the one page to read each morning
     rules.md          where the line is (templates/rules.md)
     inbox.md          only what needs you (templates/inbox.md)
     log.md            who did what, when, and where the proof is (templates/log.md)
     handoff/<job>.md  one page per job (templates/handoff.md)
     tasks/            one sheet per assignment (templates/task.md)
   ```
   If you cannot read `templates/`, create the same files from the purposes described here. No colons or slashes in file names.
3. Write "unverified" for any progress you could not find out.
4. Read every file back to confirm it exists and is right, then tell the user three things: where it is; what they can say next (e.g. "Assign: sort the files in my downloads folder by type, make a list first, don't move anything"); and what to say in a new window ("Read ai-workbench/rules.md, then take over <job>").

## 2. Assign

1. The user says in one line what they want. **Write the task sheet, save it, and read it back before doing any work** (if you get cut off, the next window can pick it up). Name it `tasks/<date>-<number>-<short-title>.md`: what to do, what done looks like (as results someone can see), which folders may be touched, what is off limits.
2. Repeat back: "I will do ... and when it is done you will see ...". Anything under rule 1 goes to the inbox to wait for the user; start the rest right away.
3. Decide what you can decide yourself and note it in the log. Only when truly stuck, add one inbox item per issue, naming the single action the user must take.
4. When finished, fill in "Actual evidence": file paths, what you saw when you opened them, whether the counts match. Set the status to "awaiting check" and update the handoff page and home page.

## 3. Check

Do this in a **new window**, ideally with a different AI. Check only; do not fix anything.

1. Go through "What done looks like" line by line and look at the real thing: does the file exist, is the content right, do the counts match, did the other side actually receive it.
2. For each line write "pass" or "fail" plus the evidence you saw. No evidence means fail.
3. All pass: set the sheet to "done". Any fail: set it to "returned" and say what is missing. Record it in the log and update the home page.
4. If you are the window that did the work, stop and tell the user to check it in another window.

## 4. Night shift

1. Start when the user says so before bed. If the client has scheduled tasks, they can schedule the same line: "Read ai-workbench/rules.md and work the night shift". This skill does not start by itself.
2. Work through task sheets marked "in progress" or "returned", and the next steps in handoff pages that do not need the user. What is off limits by day is off limits at night.
3. If something is stuck, put it in the inbox and move on to the next item. Do not sit and wait.
4. If nothing can be moved forward, write one line: "Nothing to move tonight: reason". Do not invent work to look busy.
5. Update the home page when you finish.

## 5. Handoff

- **Handing off**: when the conversation gets long, you are switching windows, or the quota is running out, update `handoff/<job>.md`: how far it got, where it is stuck, next step, where the files are, pitfalls. Write it for someone who knows nothing.
- **Taking over**: read `rules.md` and the handoff page, then check that the files it names really exist and match. Tell the user in three sentences: how far it got, where it is stuck, what you will do next. If something does not match, say so first instead of building on it. Any next step that waits for the user goes into the inbox before you report.

## 6. Morning page

Update `home.md` and show it. Four blocks only; write "none" where empty:

1. **Needs you to do** (from the inbox)
2. **Needs your decision** (from the inbox, each with one recommendation)
3. **Done and checked since last night** (with where the evidence is)
4. **Stuck or not yet checked**

When the user answers an item, move it to "Handled" in the inbox with their exact words and the date. Tentative wording ("maybe we don't need this any more?") is not a decision: reply with one yes-or-no question before acting.

## What this starter cannot do

- It does not push messages into other windows. A task sheet sits in the folder; it counts as received once the new window reads it.
- It does not start on its own. You say the word, or use your client's scheduler.
- Do not let two windows edit the same job's files at the same time.

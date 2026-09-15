---
name: follow-up-email
description: Turn pasted meeting notes into a short follow-up email recording what was agreed and what each side owes, then save it as markdown. Use when someone says "draft a follow-up email", "write up these notes as an email", "follow up on that call", or pastes meeting notes and asks for an email to the other side. Drafts only - never sends.
---

# Follow-up email from meeting notes

Turns notes from a call or meeting into a short email confirming what was agreed and what each side has to do next. It drafts; the fee earner sends. It never adds a term, a date, a concession or a name that the notes do not contain.

## Step 1 - Read what you need

Three inputs:

1. **The meeting notes**, pasted into the message.
2. **Who the email is to** - the name, and which side they are on.
3. **The deadline**, if one was agreed. If the notes agree no deadline, that is an answer; say so and carry on.

If 1 or 2 is missing, say which is missing and stop. Do not draft from one input. Do not guess who the email is for.

## Step 2 - Sort the notes

Read the notes once and put every line into one of four buckets:

- **Agreed** - both sides landed on it.
- **Ours** - something our side owes, with an owner and a date if the notes give one.
- **Theirs** - something the other side owes, same.
- **Open** - raised, discussed, parked, or left unresolved.

A thing that was *discussed* is not a thing that was *agreed*. Keep them apart. If the notes are too thin to fill **Agreed** with at least one item, or too thin to tell who owes what, stop and refuse: name which of the four buckets you could not fill and quote the lines that were too vague. Do not write a file and do not offer a skeleton with placeholders.

## Step 3 - Write the email

Keep it under 200 words. Structure:

```
Subject: <meeting or matter> - follow-up

<One line: thanks, and when the meeting was, if the notes say.>

What we agreed:
- <item>

What we will do:
- <action> - <owner> - <date or "no date agreed">

What you will do:
- <action> - <owner> - <date or "no date agreed">

Still open:
- <item>

<One closing line inviting correction.>
```

Drop any section that has no items rather than writing "none". Plain sentences, no adjectives the notes do not support, no legal characterisation of what was agreed, no "as you know" or "per our discussion". Close by asking the recipient to correct anything recorded wrongly - that line is what makes the email safe to send.

## Step 4 - Save it

Write the draft to `follow-ups/{YYYY-MM-DD}-{short-slug}.md` under the current working directory. One file, nothing else. The slug describes the meeting, not the client.

## Step 5 - Reply

In this order:

1. The full email text, so it can be read and copied without opening the file.
2. The file path.
3. Anything from the notes you deliberately left out, and why - one line each.
4. Anything the notes left unclear that the sender should check before sending.
5. The line: `Read it before you send it. This is a draft and has not been sent anywhere.`

## What this skill does not do

- Send, forward, schedule or queue an email anywhere.
- Invent a deadline, an owner, a figure, a concession or an attendee.
- Turn something discussed into something agreed.
- Add legal advice, a characterisation of the parties' obligations, or a without-prejudice or privilege label unless the notes say one was agreed.
- Write more than the one markdown file, run scripts, or reach any connector.
- Include a real client name, matter number, or any credential.

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

### Dates

Record a deadline in the words the notes used, anchored to the meeting date so
the recipient can check it: "within a week of the 11 September call", not a bare
"within a week" and not "by 18 September". Do not calculate a calendar date the
notes do not state - not in the email, and not in your reply notes either. If the
notes give a day and month but no year, do not supply the year.

### Recording something nobody has confirmed

Two different things look alike in notes. Keep them apart.

**What a person on the call said is a fact.** Record it: that they will put a
point to their client, that they could not commit, that they will come back
with an answer. "You said you would put it to your client but could not
commit" belongs under still open exactly as it happened. Never drop the fact
that someone declined to commit - that is the most important thing on the page.

**A guess about how someone who was not on the call will react is not a fact.**
"Would probably be fine with it", "can't see a problem", "should be able to
live with that". Record only the status: that it has not been put to them, or
has not been confirmed. Do not repeat the speculative words, and do not put a
position in the mouth of someone who was never asked. Write "the signage
changes have not been put to the landlord yet", not "the landlord would
probably be fine with the signage changes".

### Naming owners

On an email to the other side, the section heading already says whose action it
is, so leave the owner label off the line rather than repeating the recipient's
name. On an internal email with several owners, name each person against their
own action, because that is the whole point of the list.

Drop any section that has no items rather than writing "none". Plain sentences, no adjectives the notes do not support, no legal characterisation of what was agreed, no "as you know" or "per our discussion". Close by asking the recipient to correct anything recorded wrongly - that line is what makes the email safe to send.

## Step 4 - Save it

Write the draft to `follow-ups/{YYYY-MM-DD}-{short-slug}.md` under the current working directory. The date is the day you write the file, which you know - not the meeting date, which the notes often give without a year. One file, nothing else. The slug describes the meeting, not the client.

## Step 5 - Reply

In this order:

1. The full email text, so it can be read and copied without opening the file.
2. The file path.
3. Anything from the notes you deliberately left out, and why - one line each.
4. Anything the notes left unclear that the sender should check before sending.
5. The line: `Read it before you send it. This is a draft and has not been sent anywhere.`

## What this skill does not do

- Send, forward, schedule or queue an email anywhere.
- Invent a deadline, an owner, a figure, a concession or an attendee, or supply a calendar date or a year the notes do not give.
- Turn something discussed into something agreed.
- Add legal advice, a characterisation of the parties' obligations, or a without-prejudice or privilege label unless the notes say one was agreed.
- Write more than the one markdown file, run scripts, or reach any connector.
- Include a real client name, matter number, or any credential.

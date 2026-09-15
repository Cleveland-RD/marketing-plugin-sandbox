---
name: faq-entry
description: Turn one repeatedly asked customer question into a short website FAQ entry, using only the notes supplied and the brand/ folder, and refusing when the notes do not actually answer the question. Use when asked to "write an FAQ entry", to "turn this question into an FAQ", or to redraft an existing entry. Drafts only - never publishes to the website.
---

# FAQ entry writer

Writes one FAQ entry for the website: the customer's question as a heading, and a short answer built only from notes a colleague pastes in and facts in `brand/company.md`. It answers nothing from general knowledge. If the notes do not answer the question, it says so and writes nothing.

## Step 1 - Read the brand

Read these before drafting:

- `brand/voice.md` - spelling, punctuation, sentence shape. Required.
- `brand/banned-language.md` - phrases and punctuation that must never ship. Required.
- `brand/company.md` - the only product facts and links you may add.

If `voice.md` or `banned-language.md` is missing, stop and say which file is needed.

## Step 2 - Check you have what you need

Required before drafting:

1. **The question**, in the customer's own words.
2. **Answer notes** from whoever knows, pasted in or in a named file.

If either is missing, ask for it in the reply and stop. Ask for both in one reply. Never write the answer from what you already know about the product.

## Step 3 - Check the notes answer the question

Take the question apart into the specific things it asks. For each one, find the line in the notes or in `brand/company.md` that answers it.

Refuse and stop if any of these is true:

- The notes describe a nearby topic but never answer what was asked.
- The notes imply an answer without stating it.
- The question asks about a platform, price, or limit the notes do not name.
- Answering would need a number, date, or capability nobody supplied.

A half answer on a public page is worse than no page. Do not narrow the question so the notes happen to fit it, and do not answer the easy half and leave the rest silent. When you refuse, use the refusal shape in Step 6.

## Step 4 - Write the entry

1. **Heading.** Keep the customer's wording and framing. Fix only spelling, punctuation, and capitalisation to `brand/voice.md`. Do not rewrite the question into marketing language, and do not soften a blunt question.
2. **Answer.** Lead with the direct answer in the first sentence, yes or no where the question is a yes or no. Add the detail that makes it usable. Stop there.
3. **Length.** 40 to 100 words. One idea per entry.
4. **Facts.** Use only what is in the notes or `brand/company.md`. Copy numbers exactly as supplied, never round them. Invent no statistics, quotes, dates, or capabilities.
5. **Limits.** If the notes name a condition or exception, keep it. Dropping the exception is how an FAQ entry becomes a complaint.
6. **Link.** Add a link only if one in `brand/company.md` genuinely takes the reader further. Link to the specific page, never write "learn more".

## Step 5 - Banned-language check

1. Build the list from `brand/banned-language.md`, punctuation and patterns included.
2. Search the drafted entry for every word and punctuation entry, case-insensitive, with `grep`. Check the patterns by reading.
3. Notes pasted from a colleague often carry banned wording. Rewrite it out while keeping the fact exactly as supplied.
4. If anything hits, rewrite and check again until clean.

## Step 6 - Save and reply

Save to `content/faq/{slug}.md`, where `{slug}` is a 3-5 word kebab-case summary of the question. Put the original question verbatim in a short header above the entry so a reviewer can compare.

Reply in exactly this shape, starting with the Customer asked line. Put nothing before it, not even check results:

```
**Customer asked:** {the question exactly as it arrived}

---
## {question as heading}

{answer text exactly as it would be published}
---

**Facts used:** {one bullet per fact, naming the note line or company.md line it came from}
**Checks:** voice rules applied, banned-language check clean ({n} rules checked).
**Saved as:** content/faq/{file}.md
```

If you are refusing under Step 3, save nothing and reply in this shape instead:

```
**Customer asked:** {the question exactly as it arrived}

I cannot write this entry from these notes.

**The notes cover:** {one line on what they do say}
**The question also needs:** {the specific missing fact, named}

Send that and I will draft it.
```

If the user sends a correction, redraft the whole entry in the same shape. If the correction sounds like a permanent brand rule, add one line naming the brand file an operator should update.

## What this skill does not do

- It does not publish, schedule, or send anything to the website.
- It does not answer from general knowledge, memory, or the web.
- It does not guess, estimate, or hedge its way around a gap in the notes.
- It does not invent numbers, customer quotes, or product capabilities.
- It does not edit `brand/`.
- It does not write a token, key, or password into an entry.

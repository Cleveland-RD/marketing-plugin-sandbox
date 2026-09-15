---
name: linkedin-post
description: Draft a single LinkedIn text post for one named audience, grounded in the brand/ folder and checked against the banned-language list. Headless variant for remote agents - asks for missing information in the reply instead of an interactive question tool, and returns the post text in the reply. Use when asked to "draft a LinkedIn post", "write a LinkedIn update", or to rewrite a draft to brand. Drafts only - never publishes.
---

# LinkedIn post drafter (headless)

Adapted from the `linkedin-post` skill in Cleveland-RD/marketing-plugin v0.5.0. This pilot version keeps the drafting core and drops everything that needs a live user session: carousels, image generation, HTML and PDF rendering, the `.marketing/` memory layer, and interactive corrections.

## Step 1 - Read the brand

Read all four files before drafting:

- `brand/company.md` - facts, claims, links. Required.
- `brand/voice.md` - tone, spelling, punctuation, CTA style. Required.
- `brand/audiences.md` - named audiences, hooks, default CTAs.
- `brand/banned-language.md` - zero-tolerance phrases and patterns.

If `company.md` or `voice.md` is missing or still contains unfilled placeholders, stop and say which file needs completing.

## Step 2 - Check you have what you need

Required before drafting:

1. **Topic or angle**, in one sentence.
2. **Audience**, which must match one entry in `brand/audiences.md`.
3. **Call to action**, a specific link from `brand/company.md`. If the user gives none, use that audience's default CTA and say so.

If the topic or audience is missing or does not match, reply with a numbered list of questions and stop. Offer the audience names from `brand/audiences.md` as options. Ask everything in one reply.

If the request is only for a carousel, an image, or publishing, say this pilot agent drafts text posts only.

## Step 3 - Draft

1. Open with the audience's working day or problem, never with the company or product. Use the "hooks that work" for that audience as a guide, and avoid the "hooks that fail".
2. Write for one audience only. Do not borrow proof points aimed at another audience.
3. Apply every rule in `brand/voice.md` exactly: spelling, punctuation, sentence shape, hashtags, CTA style.
4. Use only facts, claims, and links from `brand/company.md` or stated in the request. The hooks and "what they care about" lines in `brand/audiences.md` describe the reader, not the product. Never turn them into product claims. If a request implies a capability that `company.md` does not state, leave it out and ask about it in the reply.
5. Keep it between 80 and 220 words unless the user asks otherwise.

## Step 4 - Banned-language check

1. Build the ban list from `brand/banned-language.md`, including punctuation and patterns.
2. Check the draft against every entry. For words and punctuation, run a case-insensitive search over the saved draft with `grep`. For patterns, check by reading.
3. If anything hits, rewrite and check again until clean.

## Step 5 - Save and reply

1. Save the post to `content/linkedin/{YYYY-MM-DD}-{slug}.md`, where `{slug}` is a 3-5 word kebab-case summary. Include the audience, CTA, and topic as a short header above the post text.
2. Reply in exactly this shape, starting with the Audience line. Put nothing before it, not even check results or working notes:

```
**Audience:** {audience name}
**CTA:** {link}

---
{post text exactly as it would be published}
---

**Checks:** voice rules applied; banned-language check clean ({n} rules checked).
**Facts used:** {bullet list of each product claim and the exact company.md line it came from}
**Saved as:** content/linkedin/{file}.md
```

If the user sends a correction, redraft the whole post in the same shape. If the correction sounds like a permanent brand rule, add one line naming the brand file an operator should update.

## What this skill does not do

- It does not publish, schedule, or email anything.
- It does not create carousels, images, HTML previews, or PDFs.
- It does not invent customer quotes, statistics, awards, or product facts.
- It does not edit `brand/`.

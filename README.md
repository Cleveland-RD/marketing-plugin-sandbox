# harbourline-marketing (pilot sandbox)

Synthetic plugin for the Cleveland & Co agent pilot. It exists so the skill
builder has a realistic target to open pull requests against.

**Everything in this repository is invented.** Harbourline Legal Software is a
fictional company. No client material, no firm intellectual property, and no
real brand content belongs here, and none is present.

## Layout

```
.claude-plugin/plugin.json      plugin manifest
skills/<name>/SKILL.md          one skill per folder
evals/<name>/<case>/prompt.md   test cases, at the repository root
brand/                          synthetic brand facts the skills read
```

Eval cases must sit under `evals/` at the root. `claude plugin eval` refuses an
eval directory inside `skills/`.

## How changes arrive

A colleague describes a job in Claude Cowork. The builder agent drafts the
skill and its test cases, runs validation and a client-identifier scan, and
opens a pull request. A maintainer reviews and merges. The builder cannot
merge, and that restriction is enforced by the ruleset on `main`.

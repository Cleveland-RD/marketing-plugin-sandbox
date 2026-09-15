This case expects the skill to write one markdown file under `follow-ups/`.
Whoever runs the suite must pass `Write` to the eval runner, or the case fails
on a permission the skill never had. The same applies to
`internal-project-call` and `discussed-not-agreed`.

`vague-notes-refusal` and `missing-recipient` expect no file to be written and
run correctly without `Write` granted.

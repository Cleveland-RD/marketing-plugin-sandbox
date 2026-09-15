---
max_turns: 10
# This case exercises the save step, so the suite must grant Write:
#   claude plugin eval --allow Write
allowed_tools: [Read, Glob, Grep, Skill, Write]
---

Turn this question into an FAQ please.

Question: "How long does onboarding take before our team can actually use it?"

Notes from the implementation lead: a standard rollout takes 12 working days
from contract to first formatted document. That covers capturing the house
style, a test batch of 5 documents, and one training session. Firms with more
than one house style should expect 18 working days. We do not offer a same-week
rollout.

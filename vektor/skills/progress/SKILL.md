---
name: progress
description: Show the learner's vektor.fm mission progress. Invoke only when the user explicitly runs /vektor:progress.
disable-model-invocation: true
---

Read `~/.vektor/progress.json` (on Windows: `$HOME/.vektor/progress.json`).
Do not modify it.

If the file doesn't exist: tell the learner they haven't started yet
and that `/vektor:start` begins Mission 01 (~25 min).

If it exists, render their status as a compact tree, exactly this shape:

VEKTOR.FM — YOUR PROGRESS
  [✓/▶/ ] 01 Token Discipline        <cleared DATE / in progress, step N of 5 / not started>
  [ ] 02 (coming soon)
  [ ] 03 (coming soon)

Legend: ✓ cleared, ▶ in progress, blank not started.

- If mission 01 is in progress: remind them `/vektor:start` resumes
  exactly where they left off.
- If mission 01 is cleared: one short congratulation (no gushing) and a
  note that new missions are announced at vektor.fm.
- Never inflate: report only what the file says.

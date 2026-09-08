# Notes for me

Working notes on writing skills here and contributing them onward.

## Writing a skill

Structure of the body, in order:

1. When it applies — one line.
2. What it produces — one line.
3. The procedure, in `##` sections.
4. `## What good looks like` — required.
5. Hard rules (MUST / NEVER) — last.

Around 600 words. Terse. No vendor tool names anywhere — use plain commercial verbs like "pull the pipeline export", "load the orders figures", because the reader's stack is unknown.

Deeper material — worked examples, frameworks, variants — goes in `references/<topic>.md`, and the body says when to read it.

The `description` field in the frontmatter is what makes a skill trigger at all. Pack it with the phrases someone would actually type when they need it.

## What gets a skill rejected

The bar is judgment, not process. A skill that only lists steps gets rejected. The parts that carry weight:

- What you notice first that others miss.
- What the mediocre version of this looks like.
- How you know the output is good.

That's what `## What good looks like` is for.

## Confidentiality line

Encode the method, never the numbers. No margin floors, discount thresholds, cover ratios or portfolio mix figures from an employer. Write "test whether the gap closes on term extension before touching list price", not the actual threshold.

## Contributing a skill to gtmskills.com

The library lives at `swan-gtm/gtm-skills` on GitHub. Maintained by Swan, MIT licensed, reviewed by a maintainer before it goes live.

Because this repo uses the same folder layout, the files copy across as-is.

Browser route, no terminal needed:

1. Fork `github.com/swan-gtm/gtm-skills`.
2. In the fork, "Add file → Create new file". Type the full path with slashes in the filename box and GitHub creates the folders: `skills/leret-mutkut/<skill-name>/SKILL.md`.
3. Do the same for `skills/leret-mutkut/author.md` — first submission only.
4. Commit to a new branch.
5. "Contribute → Open pull request" back to the original repo. Fill in their checklist.

Before submitting, check the category is one they already use:

```bash
grep -h "^category:" skills/*/*/SKILL.md | sort -u
```

Their checker is `node tools/validate.mjs`. It can't be run in the browser, but their automated checks run it on the pull request and report failures, so fix and re-commit if it complains.

No git at all? Open a "Submit a skill" issue on their repo and paste both files into the form. A maintainer converts it into a pull request.

Review gates on their side: conventions and completeness, security, voice and judgment, author identity, publish.

## Author profile

`skills/leret-mutkut/author.md` — the folder name is the permanent public slug. Frontmatter takes `name`, `avatarUrl`, `title`, `linkedinUrl`, `companyDomain`. The bio is the body text.

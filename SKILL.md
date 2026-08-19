---
name: noclaudism
description: >
  Rewrites text from Claude's house style into plain English: removes the
  verbal tics the community calls Claude-isms (load-bearing, footgun,
  "you're absolutely right", "one honest caveat", "not X but Y") while
  keeping every fact intact. Use when the user says "noclaudism",
  "de-claude this", "remove the Claude-isms", "translate from Claudish",
  "plain English pass", "make this sound human", asks to clean AI tics
  from a reply, a file, a commit message, a PR description, or a
  document, or asks why the text reads like it was written by a machine.
---

# noclaudism

Rewrite the given text, or the given file, into plain English. Keep
every fact, number, name, file path, and code block exactly as it was.
Remove the style, not the substance.

The style being removed has two layers. The first is fake social
behavior: praise the reader did not ask for, agreement announced before
content, honesty announced instead of practiced. The second is a
private vocabulary of metaphors and frames that the writer treats as
shared language when the reader never agreed to it. Both layers make a
reader work to find out what actually happened.

## The moves

Work through the text with these rules. Deleting beats replacing:
most tics carry no information, so the right fix is removal, and the
sentence that remains must stand on its own.

**Delete the social layer.** Openers like "You're absolutely right",
"Great question", "Good catch", "Fair point", "That's a valid concern"
come out whole. If the user was right about a fact, the rewrite shows
it by stating the fact.

- Before: "You're absolutely right, and that changes the scope of this
  task in a meaningful way. The parser does skip empty lines."
- After: "The parser does skip empty lines, so the task changes."

**Delete announced honesty.** "Honestly", "to be honest", "my honest
take", "let me be direct", "real talk", "one honest caveat", "full
stop". A direct sentence does not need a permit. If everything else
was honest too, the announcement was noise; if it was not, the
announcement was worse.

- Before: "Honestly? The migration script is the riskier half, and
  that's worth sitting with."
- After: "The migration script is the riskier half."

**Delete importance frames.** "The key insight is", "what actually
matters here", "crucially", "worth noting", "worth flagging", "the
crux", "the kicker", "why this matters". Delete the frame and keep
what was inside it. If the content is important, it survives on its
own; if the sentence collapses without its frame, the frame was the
content, and nothing is lost.

**Replace the metaphor lexicon with the concrete fact.** Words like
load-bearing, footgun, seam, spine, blast radius, smoking gun,
guardrails, escape hatch, belt-and-suspenders, happy path, landmine
each stand in for something specific the writer knew and did not say.
Say the specific thing, in the domain's own words.

- Before: "This check is load-bearing: removing it is a footgun with a
  wide blast radius."
- After: "Three call sites depend on this check. Removing it breaks
  session refresh, logout, and the tests that cover both."

The full catalog with replacements is in `references/claudisms.md`.
Read it when auditing a text, and whenever unsure whether a phrase is
a tic or a term the domain actually uses. A term the reader's field
genuinely uses (defense-in-depth in security, happy path in testing)
may stay when the audience is that field.

**Unwind the contrast reflex.** "It's not X, it's Y" and "this isn't
just X, it's Y" become a sentence about Y. Keep the contrast only when
someone actually claimed X and the difference decides something.

**Cut epigrams and offers.** The short closing thump ("That's the
whole story.", "And that's not nothing.") comes off; the paragraph
ends on its last fact. Sign-off offers ("Want me to keep going?",
"Say the word", "Happy to elaborate") come out unless the text
genuinely needs a decision from the reader, in which case ask a plain
question naming the decision.

**Dissolve the skeleton.** When every reply has the same shape
(warm opener, three bullets, a caveat, an offer), the shape itself is
a tic. Let the content pick the shape: one finding is one paragraph,
a list of four files is a list, a decision needing input ends with the
question.

**Retire private shorthand.** A name coined earlier in a conversation
or document ("the parity bench", "the doctrine", "the 74.5% problem")
is not shared vocabulary. Either say what the thing is in ordinary
words, or introduce the name properly once and use it consistently.
The test for every sentence: would it make sense, read aloud, to
someone who was not there when the shorthand was coined?

**Keep sentences whole.** An actor, a verb, everyday words. Split
noun-pile inventories into sentences with subjects. Passive voice
becomes active where an actor exists: "the file is opened by the
loader" becomes "the loader opens the file".

## What never changes

- Facts, measurements, version numbers, dates, names, file paths.
- Code blocks, commands, quoted error messages, and identifiers.
- Real uncertainty. A genuine hedge stays, stated plainly: "I did not
  test the Windows path" survives, "it should probably work modulo
  edge cases worth flagging" does not.
- Meaning. When a tic carries real information (the writer knew which
  three call sites break), the rewrite states that information rather
  than deleting it. When the information is not in the text and cannot
  be recovered, keep the claim general rather than inventing details.

## Procedure

**Rewriting a passage the user gives directly:** output only the
rewritten text. No preamble, no commentary on the changes, unless the
user asks what changed.

**Rewriting a file:** read the whole file first. Rewrite prose;
leave code blocks, front matter, tables of data, and link URLs alone.
Write the result back to the same file when the user said to change
it, or to a sibling copy when they asked to keep the original. Report
in one or two sentences what was done, in plain English.

**Auditing without rewriting:** when the user asks what is wrong with
a text rather than for a rewrite, list each tic found with a line
number or quote and the category it belongs to, then offer the
rewrite as a next step in one short sentence.

**Commit messages and other one-liners:** one sentence, active voice,
says what a user of the software gains or what changed. Internal
machinery is named only when the machinery is the deliverable.

- Before: "feat: CBR comics through rarball, compressed and damaged
  archives refuse by name"
- After: "feat: open CBR comic books, with a clear message when a
  file is broken, encrypted or compressed"

## Example

Before:

> You've hit on something meaningful here. The auth check isn't just a
> guard clause, it's load-bearing: the whole session lifecycle leans on
> it, and removing it would be a real footgun. Honestly? My
> recommendation is to keep it, full stop. One honest caveat worth
> flagging: the check quietly swallows timeout errors, which is a rough
> edge worth knowing about. Want me to write up a fix? Just say the
> word.

After:

> Keep the auth check. Session refresh, logout, and token renewal all
> call it, and removing it breaks all three. It has one bug: it
> catches timeout errors and drops them without logging. I can fix
> that if you want.

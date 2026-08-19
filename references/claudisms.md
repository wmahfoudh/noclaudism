# The catalog

The tics, grouped by what they pretend to do. Use this as a scan list
when auditing a text and as a lookup when unsure whether a phrase is a
tic. The fix column gives the usual repair; "delete" means the phrase
carries nothing and the sentence stands without it.

A phrase on this list is not banned everywhere. Some entries are real
terms in specific fields ("happy path" in testing, "defense in depth"
in security) and may stay when written for that field. The question is
always whether the reader gains anything from the phrase, and banning
words alone does not work anyway: a writer who loses "load-bearing"
reaches for "the crux" unless the habit behind the word changes. The
habit is what the skill's moves address; this list is for finding
instances, not for curing the disease one word at a time.

## Fake agreement and praise

Delete these whole. If the user was right, show it by stating the fact
they were right about.

- "You're absolutely right"
- "Great question" / "Great catch" / "Good catch" / "Sharp catch"
- "You've hit on something meaningful"
- "Your instinct is right" / "Good instinct"
- "Fair point" / "That's fair"
- "That's a valid concern" / "perfectly reasonable"
- "Exactly right" / "Spot on"
- "You're right to push back" / "You're right to flag this"
- "That's the most honest thing anyone's said in this conversation"

A related move invents a misunderstanding the reader never had in
order to correct it, or "gently pushes back" on something nobody
claimed. Delete the invented disagreement and answer what was asked.

## Announced honesty

Delete. Directness is shown, not declared, and the announcement
implies everything else was less than honest.

- "Honestly" / "And honestly?" / "to be honest"
- "My honest take" / "my honest read" / "the honest answer"
- "One honest caveat" / "one honest limitation" / "a real caveat"
- "Let me be direct" / "let me be blunt" / "let me put it plainly"
- "Real talk" / "straight answer" / "no hand-waving"
- "Full stop." / "Period." as sentence enders
- "Let me ground myself" / "grounded in what's actually in the repo"

## Importance frames

Delete the frame, keep the content. If the sentence collapses without
its frame, the frame was hiding that there was no content.

- "The key insight is" / "the crux" / "the core issue"
- "What actually matters" / "the decision that actually matters"
- "Crucially" / "importantly" / "notably" / "tellingly"
- "Worth noting" / "worth flagging" / "worth calling out" /
  "worth knowing about" / "worth sitting with"
- "The kicker" / "the punchline" / "the tell" / "the bottom line"
- "Why this matters:"
- "Here's the through line"
- "This changes everything" / "and that changes the picture"

## The metaphor lexicon

Replace with the concrete fact the metaphor stands for. The middle
column is what the writer usually means; say that, in the domain's
words, with the specifics if they are known.

| Tic | What it usually means |
|---|---|
| load-bearing | other code depends on this; removing it breaks named things |
| footgun | easy to misuse; the misuse causes a specific failure |
| seam | a boundary between two parts; an interface |
| spine / backbone | the part the rest is organized around |
| shape (of a problem) | the structure; the outline; what kind of problem it is |
| blast radius | what else changes or breaks |
| smoking gun | the evidence that identifies the cause |
| guardrails | checks that prevent a specific mistake |
| escape hatch | a way to bypass or opt out |
| belt-and-suspenders / belt-and-braces | two redundant safeguards |
| landmine / minefield | a hidden hazard; code that fails when touched |
| happy path | the case where nothing goes wrong |
| gotcha | a surprising behavior |
| under the hood / the plumbing | in the implementation |
| workhorse / does the heavy lifting | the part that does most of the work |
| earns its keep / earns its place | is justified by what it does |
| quietly swallows / silently drops | discards without logging or reporting |
| battle-tested | widely used for a long time |
| the culprit / the offending line | the cause; the line with the bug |
| linchpin / hinge | the part everything else depends on |
| canonical | the standard or agreed-upon one |
| surface area | the amount exposed; the number of entry points |
| north star | the goal |
| lever | a way to influence something |
| moat | a durable advantage |
| soak / soak time | running unchanged for a while to build confidence |
| sanity check | a quick check that the result is plausible |
| lands / landed | happened; was merged; had the intended effect |

## Structure tics

- "It's not X, it's Y" / "This isn't just X, it's Y": say Y. Keep the
  contrast only when someone actually claimed X.
- The rule of three: three parallel phrases where one precise one
  would do.
- The closing epigram: a short summarizing thump at the end of a
  paragraph ("That's the whole story.", "And that's not nothing.").
  End on the last fact instead.
- The caveat epilogue: a final paragraph of qualifications opened
  with "One thing worth flagging". If a caveat matters, it belongs
  where the claim was made; if it does not, it goes.
- Sign-off offers: "Want me to...?", "Say the word", "Just let me
  know", "Happy to elaborate". Ask a plain question when a decision
  is genuinely needed; otherwise stop writing.
- The fixed skeleton: warm opener, three bullets, caveat, offer, on
  every reply regardless of content.
- Adverb inflation: "actually", "genuinely", "arguably",
  "empirically", "concretely" sprinkled as emphasis. Delete; they
  weaken the sentence they decorate.
- "quietly" / "silently" attached to verbs for drama rather than to
  report missing logging.
- Em-dash chains splicing three thoughts into one sentence. Split
  into sentences.
- Two-word sentence fragments as paragraphs. For emphasis. Like this.

## Private shorthand

The writer coins a name ("the parity bench", "the doctrine", "the
74.5% problem") or promotes a stray number or phrase into slang, then
uses it as if the reader had agreed to the vocabulary. Repair: say
what the thing is in ordinary words, or introduce the name once,
properly, and use it consistently. The read-aloud test catches these:
the sentence must make sense to someone who was not present when the
name was coined.

## One-liners: commits, PR titles, changelog entries

The compressed forms of all of the above meet in commit messages:
noun piles, coined names, passive voice, machinery instead of effect.
One sentence, active voice, what changed or what the user gains.
Name internal machinery only when the machinery is the deliverable.

- "refactor: one haystack, two matchers ready" becomes "refactor:
  prepare the search text so both match modes can share it"
- "feat: the book bar measured, tier rows, parity bench and the
  corpus sweep" becomes "feat: performance tests for the book
  formats"

## Sources

The catalog draws on community threads that named and collected these
patterns, and on corrections collected from real sessions:

- r/ClaudeAI, "Claude Code plugin for translating from Claudish to
  English" (reddit.com/r/ClaudeAI/comments/1vl0n1t)
- r/ClaudeAI, "Gaslighting Claude with its own Verbal Tics"
  (reddit.com/r/ClaudeAI/comments/1vrlrud)
- r/ClaudeAI, "Favorite claude-isms in no particular order"
  (reddit.com/r/ClaudeAI/comments/1v33cab)
- r/ClaudeAI, "Anybody have a good method to tone down the
  Claude-isms?" (reddit.com/r/ClaudeAI/comments/1vr7bqj)

The threads also record two findings this skill's design follows:
word ban lists fail because the habit finds synonyms, and style
instructions fade as a conversation grows. A rewrite pass invoked
fresh, like this skill, does not fade, and example pairs teach better
than prohibitions.

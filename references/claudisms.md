# The catalog

The tics, grouped by what they pretend to do. Use this as a scan list
when auditing a text and as a lookup when unsure whether a phrase is a
tic. The fix column gives the usual repair; "delete" means the phrase
carries nothing and the sentence stands without it.

A phrase on this list is not banned everywhere. Some entries are real
terms in specific fields ("happy path" in testing, "defense in depth"
in security, "gate" in CI pipelines) and may stay when written for
that field. The question is always whether the reader gains anything
from the phrase, and banning words alone does not work anyway: a
writer who loses "load-bearing" reaches for "the crux" unless the
habit behind the word changes. Nor does rewording a tic into plain
English cure it: "ready for production" is "production-ready" in a
plainer coat. The habit is what the skill's moves address; this list
is for finding instances, not for curing the disease one word at a
time.

## Fake agreement and praise

Delete these whole. If the user was right, show it by stating the fact
they were right about.

- "You're absolutely right" / "You're right, and it's not even close"
- "Great question" / "Great catch" / "Good catch" / "Sharp catch"
- "Sharp observation" / anything the reader said graded "sharp"
- "You've hit on something meaningful" / "you've touched on something
  real" / "that pain is real"
- "Your instinct is right" / "Good instinct"
- "Fair point" / "That's fair" / "that's a fair question"
- "That's a valid concern" / "perfectly reasonable"
- "Exactly right" / "Spot on" / "That tracks"
- "You're right to push back" / "You're right to flag this"
- "You're identifying the exact right tension"
- "You just buried the lede"
- "Both are true" / "both can be true" (followed by restating both)
- "And honestly? That's rare."
- Superlatives about the reader: "That's the most honest thing
  anyone's said in this conversation", "the sharpest observation in
  the thread", "I've never seen such an elegant solution"

Grading by halves is the same tic with a verdict attached: "You're
half right, and the half where you're wrong is the interesting part."
Either state which part is right and which is wrong, with the reason,
or delete the sentence. A verdict on the reader with no specifics
behind it carries nothing, and rewording it ("part of what you said
is right, part is wrong") does not save it.

## Manufactured disagreement

When nothing needs correcting, the style invents something to correct:
a misunderstanding the reader never had, a "gentle pushback" against a
claim nobody made, a diagnosis of the reader's behavior, or a decision
attributed to the reader that the writer proposed. Delete the invented
disagreement and answer what was asked. Correct only claims that were
actually made, by stating the fact.

- "Let me gently push back" / "one thing I'd push back on"
- "I want to stop you right there"
- "one thing you probably can't see from the inside"
- "We've circled this three times now"
- "You previously decided X" (when the writer suggested X)

## Apology theater

A mistake gets a confession scene: self-blame, a moral, a promise. The
repair is one sentence saying what went wrong and what changes, then
the fix. No verdict on oneself, in any wording: "that was my mistake"
is "that's on me" restated.

- "You're absolutely right. I should have checked before assuming."
- "and that's on me" / "that was my mistake" as a closing moral
- "I was wrong earlier, and I'm sorry about that"
- "I owe you a straight account, not excuses"
- Grandiose damage narration: "a catastrophic error that rendered the
  files completely and totally irretrievable" for a failed copy. Say
  what was lost and what is recoverable.

## Announced honesty

Delete. Directness is shown, not declared, and the announcement
implies everything else was less than honest.

- "Honestly" / "And honestly?" / "to be honest"
- "My honest take" / "my honest read" / "the honest answer" /
  "the honest truth" / "honest framing"
- "One honest caveat" / "one honest limitation" / "a real caveat" /
  "a genuine caveat"
- ", said honestly" / ", stated honestly" as sentence suffixes
- "Let me be direct" / "let me be blunt" / "let me put it plainly"
- "I need to be honest with you" / "I'm going to be honest here,
  because you deserve it"
- "Real talk" / "straight answer" / "no hand-waving"
- "The short answer:" (followed by a long answer)
- "Full stop." / "Period." as sentence enders
- "Let me ground myself" / "grounded in what's actually in the repo"

## Importance frames

Delete the frame, keep the content. If the sentence collapses without
its frame, the frame was hiding that there was no content.

- "The key insight is" / "the crux" / "the core issue" /
  "the real question"
- "What actually matters" / "the decision that actually matters" /
  "and that matters"
- "Crucially" / "importantly" / "notably" / "tellingly"
- "Worth noting" / "worth flagging" / "worth calling out" /
  "worth knowing about" / "worth sitting with" / "worth naming"
- "naming" as an intellectual act: "the pattern you're naming",
  "names the problem". Say, show, or display it instead
- "Sit with it" / "the thing to hold onto"
- "Know this cold" / "Lock it in"
- "The kicker" / "the punchline" / "the tell" / "the bottom line"
- "Why this matters:"
- "Here's the through line"
- "This changes everything" / "that changes the picture" /
  "that reframes everything"

## Hedging connective tissue

Transitions that fake a turn or soften a sentence that needed no
softening. Delete unless the sentence actually reverses direction.

- "That said" / "Having said that"
- "To be fair"
- "If anything"
- "non-trivial" (say how hard, or drop)

## Self-grading

The writer grades their own work instead of describing it. Delete the
grade and keep the description. A status claim ("done",
"production-ready") survives only next to its evidence: what ran,
what passed. When the evidence is not in the text, say what was done
and stop; do not launder the grade into plain words ("ready for
production", "catches real failures").

- "clean" / "cleanly" / "I'll do this cleanly"
- "elegant" / "tight" / "sharp" about one's own output
- "production-ready" / "robust" as bare assertions
- "the test suite has teeth"
- "Now I have the complete picture" / "the full picture"
- "We've landed the fix" / "the fix landed"
- "The result is decisive"
- "with a clear message" / "a helpful error": the message grading
  itself. State what the message says, or use the domain's phrase:
  "compressed files are not supported"

## Personification

Data gets a mind: contents "decide", an archive "says so", a function
"wants", a config "knows". The habit usually appears while escaping
passive voice: the real actor (the program, the writer) was dropped,
so something inanimate is promoted into the subject slot and handed a
verb of thought. Name the real actor, or keep a plain passive when
the actor is obvious or beside the point. A program performing its
function stays active ("Oryx opens the archive", "the parser skips
empty lines"); data does not decide, know, say, want, or believe.

- Before: "The file's content decides how it opens, not its name."
- After: "Files are interpreted by their content, because the
  extension is often misleading."

Naming the actor is not a license to put it everywhere or to hand it
drama. A program that is the subject of every sentence ("Oryx opens...
Oryx reports... it refuses...") is a skeleton of its own;
documentation keeps plain passives when the actor is obvious. And the
program's verbs stay ordinary: shows, displays, reads, reports. Where
the field has a standard phrase, use it: "compressed files are not
supported" beats "it refuses the compressed one".

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
| scope | what a task includes and excludes; filler when everything is a scope |
| tension | an unresolved trade-off between two named things |
| blast radius | what else changes or breaks |
| smoking gun | the evidence that identifies the cause |
| guardrails | checks that prevent a specific mistake |
| gate | a required check before something proceeds |
| teeth (checks with) | actually fails or blocks when violated |
| escape hatch | a way to bypass or opt out |
| belt-and-suspenders / belt-and-braces | two redundant safeguards |
| landmine / minefield | a hidden hazard; code that fails when touched |
| happy path | the case where nothing goes wrong |
| gotcha | a surprising behavior |
| under the hood / the plumbing | in the implementation |
| workhorse / does the heavy lifting | the part that does most of the work |
| earns its keep / earns its place | is justified by what it does |
| quietly swallows / silently drops | discards without logging or reporting |
| falls through the cracks | gets missed |
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
| pressure-test | check against hard or adversarial cases |
| lands / landed | happened; was merged; had the intended effect |
| ship / ship it | release it; merge it; deliver it |
| closes the gap | removes the difference; fixes what was missing |
| here's where it bites | the specific failure this causes |
| contract | what one part promises another; an interface |
| wrinkle | a complication |
| calculus | the trade-off; what decides the choice |
| orthogonal | independent; unrelated |
| chicken-and-egg | a circular dependency |
| spaghetti | tangled, hard-to-follow code |
| cargo cult | copying the form without the reason |
| dogfood / dogfooding | using your own product |
| hand-wavy | vague; missing the actual mechanism |
| legible | understandable at a glance |
| in-flight | currently running; not yet finished |

## Stock anecdotes and costumes

A borrowed story or disguise image stands in for a plain statement.
Replace it with the things compared and the property they share.

- "turtles all the way down": the explanation is circular; say what
  repeats
- "eating the elephant one bite at a time": do it in small steps;
  name the first step
- "a feature, not a bug": intentional; say why
- "MacGyver it": improvise with what already exists
- "X in a trench coat" / "two things wearing the same hat" /
  "cosplaying as" / "the same church with different pews": name the
  two things and what they actually share

## Structure tics

- "It's not X, it's Y" / "This isn't just X, it's Y": say Y. Keep the
  contrast only when someone actually claimed X.
- "X over Y" aphorisms ("Honesty over sunk cost"): state the actual
  decision and its reason.
- The rule of three: three parallel phrases where one precise one
  would do.
- The closing epigram: a short summarizing thump at the end of a
  paragraph ("That's the whole story.", "And that's not nothing.",
  escalated as "That's not nothing. That might actually be
  everything."). End on the last fact instead.
- The caveat epilogue: a final paragraph of qualifications opened
  with "One thing worth flagging". If a caveat matters, it belongs
  where the claim was made; if it does not, it goes.
- Sign-off offers: "Want me to...?", "Say the word", "Just let me
  know", "Happy to elaborate". Ask a plain question when a decision
  is genuinely needed; otherwise stop writing.
- "Verdict:" / "TL;DR:" stamps on a short text: a text short enough
  to end with its own summary did not need one.
- Care-talk closers: "Get some rest", "Seriously, go to bed", "You've
  done enough today", "How does that land with you?". Delete; end on
  the last fact.
- Manufactured homework: "Two questions are genuinely yours to
  answer:". Ask only decisions the work actually needs, as plain
  questions.
- The fixed skeleton: warm opener, three bullets, caveat, offer, on
  every reply regardless of content.
- The drama pause: "Wait." / "Oh." / "Let me pause here" / one-word
  and two-word paragraphs, for effect. Like this. Delete; the reader
  sets their own pace.
- Preterition: "I won't insult you by explaining X", followed by
  explaining X. Explain or don't.
- Answering a yes-or-no question with "(Adverb) so.": say yes or no.
- Circular framing: "There's one thing I need to tell you, and I need
  to tell you because it's important."
- Adverb inflation: "actually", "genuinely", "arguably",
  "empirically", "concretely" sprinkled as emphasis. Delete; they
  weaken the sentence they decorate.
- Bold sprinkled on single words for emphasis. Unbold; the sentence
  carries the weight or it does not.
- "quietly" / "silently" attached to verbs for drama rather than to
  report missing logging.
- Em-dash chains splicing three thoughts into one sentence. Split
  into sentences.

## Private shorthand

The writer coins a name ("the parity bench", "the doctrine", "the
74.5% problem") or promotes a stray number or phrase into slang, then
uses it as if the reader had agreed to the vocabulary. The coined
framework is the same habit in compound form: a hyphenated frame
invented on the spot and treated as established ("the
'intuition-as-colonoscopy' path", "the bootstrap-as-séance problem").
Repair: say what the thing is in ordinary words, or introduce the
name once, properly, and use it consistently. The read-aloud test
catches these: the sentence must make sense to someone who was not
present when the name was coined.

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
- r/ClaudeAI, "Claude hook to remove known Claude-isms"
  (reddit.com/r/ClaudeAI/comments/1vmqjod)
- r/claudexplorers, "What are your favorite Claude-isms?"
  (reddit.com/r/claudexplorers/comments/1rex1lk)
- r/claudexplorers, "Claude-isms I Love"
  (reddit.com/r/claudexplorers/comments/1spqf7f)
- r/RedditAlternatives, "Warning: rhyme.com is not what it pretends
  to be", where Claude-isms in a site's prose outed it as
  machine-written despite its anti-AI branding

The threads record three findings this skill's design follows. Word
ban lists fail because the habit finds synonyms. Style instructions
fade as a conversation grows, while a rewrite pass invoked fresh does
not, and example pairs teach better than prohibitions. And word-level
substitution (regex hooks, a generic "simplify" instruction) leaves
the reply's structure intact and tends to make text vaguer; the tell
is the skeleton as much as the vocabulary, and the repair must move
toward the concrete fact, never away from it.

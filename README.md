# noclaudism

**This README is written by Claude**

A skill for Claude that rewrites Claude's own output into plain
English.

Claude writes well-formed sentences in a style many people find hard
to read: praise nobody asked for, honesty announced instead of
practiced, and a private vocabulary of metaphors. Everything is
load-bearing, every risk is a footgun, every reply opens with "You're
absolutely right" and closes with "one honest caveat". The community
named this dialect Claudish, collected its phrases in long Reddit
threads, and built translators for it. This skill is one of those
translators, written as instructions Claude follows rather than as a
second model watching the first.

Two findings from those threads shaped the design. Banning words does
not work, because the habit behind the word finds a synonym: remove
"load-bearing" and "the crux" appears. And style instructions placed
at the start of a session fade as the conversation grows. So this
skill is not a standing instruction. It is a rewrite pass, invoked
fresh each time, built on principles and example pairs instead of a
ban list.

## What it does

Given a passage, a file, or its own previous reply, Claude rewrites
the prose so that:

- fake agreement and praise are gone
- "honestly", "let me be direct" and their family are gone
- metaphors are replaced by the concrete fact they stood for
- "it's not X, it's Y" becomes a sentence about Y
- closing offers and summarizing one-liners are gone
- every sentence has an actor and a verb

Facts, numbers, names, file paths, code blocks, and quoted errors are
kept exactly. Real uncertainty stays, stated plainly.

It also covers the compressed forms of the same style: commit
messages, PR titles, and changelog entries become one active sentence
about what changed.

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

## Install

For Claude Code, clone this repository into your skills folder:

```
git clone https://github.com/wmahfoudh/noclaudism ~/.claude/skills/noclaudism
```

New sessions pick it up automatically. Any other harness that reads
skill folders with a `SKILL.md` works the same way.

## Use

- `/noclaudism` followed by text rewrites that text.
- "Rewrite your last answer with noclaudism."
- "Run noclaudism on README.md."
- "Audit this file for Claude-isms" lists what it finds without
  rewriting.

## What is in the repository

- `SKILL.md`: the instructions Claude follows, with the rewrite moves
  and examples.
- `references/claudisms.md`: the catalog of tics, grouped by what
  they pretend to do, with plain replacements for the metaphor
  vocabulary, and links to the community threads it draws on.

## Contributing

The catalog grows from real examples. If Claude writes something at
you that belongs in it, open an issue with the phrase and, if you
have one, the plain version you wanted.

## License

MIT.

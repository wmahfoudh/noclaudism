# noclaudism

**Claude wrote this README**

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

Three findings from those threads shaped the design. Banning words
does not work, because the habit behind the word finds a synonym:
remove "load-bearing" and "the crux" appears. Style instructions
placed at the start of a session fade as the conversation grows. And
word-level substitution, whether a regex hook or a generic "simplify"
instruction, leaves the reply's structure intact and tends to make
text vaguer rather than plainer. So this skill is not a standing
instruction and not a word list. It is a rewrite pass, invoked fresh
each time, built on principles and example pairs, and its repairs move
toward the concrete fact.

## What it does

Given a passage, a file, or its own previous reply, Claude rewrites
the prose so that:

- fake agreement, praise, and grades on the reader are gone
- invented pushback and confession scenes over mistakes are gone
- "honestly", "let me be direct" and their family are gone
- metaphors and stock anecdotes are replaced by the concrete fact
  they stood for
- self-grades like "clean" and "production-ready" become a
  description of what the work does, with evidence when there is any
- "it's not X, it's Y" becomes a sentence about Y
- data stops thinking: contents that "decide" or "know" get a real
  actor or a plain passive
- closing offers, verdict stamps, and care-talk sign-offs are gone
- every sentence has an actor and a verb

The rewrite keeps facts, numbers, names, file paths, code blocks, and
quoted errors exactly as they were. Real uncertainty stays, stated
plainly.

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

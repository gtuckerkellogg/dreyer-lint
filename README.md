# Dreyer lint

[Dreyer's English](https://www.amazon.com/Dreyers-English-Utterly-Correct-Clarity/dp/0812995708) is indispensable for my writing and editing. The [Vale](https://github.com/errata-ai/vale) linter provides a framework for using a user-provided style with an efficient linter. I write in [Emacs](https://www.gnu.org/software/emacs/), for which a [Flycheck integration for Vale](https://github.com/abingham/flycheck-vale) is available, so I'm re-reading Dreyer's English and putting together a Vale style based on my interpretation of Dreyer's recommendations.

## Very much a work in progress

This is very much a work in progress. I'm implementing chapter by chapter, and learning about Vale at the same time.  What counts as an error and what counts as a suggestion are subject to change.

## Example: "pretty much", or "pretty good". 

Dreyer recommends avoiding this sort of usage, but doesn't recommend avoiding "pretty" in general. I thought at first that I could use Vale's Part of Speech (POS) tagging to avoid "pretty" when followed by an adjective or adverb, but Vale's current support for POS tagging is limited to substitution rules, not existence rules. So I downloaded the top 1,000,000 two-word n-grams in English from <https://www.ngrams.info/>, and identified 229 cases of "pretty"  followed by an adjective or adverb, all of which are now in `pretty.yml`.

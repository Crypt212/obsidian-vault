# Regular Expressions
- are a formal notation that defines a [[Regular Languages|regular language]].
- specifies a pattern that can be matched by strings over a given alphabet.
## Rules (Grammar)
- $0\ and\ 1$: Match the literal characters 0 and 1.
- $ε$: Represents the empty string.
- $(r_1)+(r_2)$: Union (logical OR) e.g., 0 + 1 means 0 or 1. (old alternative: $(r_1)|(r_2)$
- $(r_1)(r_2)$: Concatenation of two regular expressions.
- $(r)^*$: Kleene star zero or more repetitions of r.
- $(r)+$ : One or more repetitions of r.
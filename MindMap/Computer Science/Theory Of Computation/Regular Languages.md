Regular Languages: These are the simplest class of languages in the
Chomsky hierarchy, and they can be defined using **regular expressions**
or recognized by [[finite automata]].
# Regular Expressions
- are a formal notation that defines a regular language.
- specifies a pattern that can be matched by strings over a given alphabet.
# Formalizing
- let $L$ be a function that maps any **regular expression** to the **regular language** that it generates, this function takes:
	- **Input**: A regular expression $R$
	- **Output**: The language $L(R) \subseteq \Sigma^*$ (set of all strings matching $R$)
- it has some properties:
- $L(\varepsilon) = {\varepsilon}$
- $L(a) = {a}, \forall a \in alphabet\ \Sigma$
- $L(R_1|R_2) = L(R_1) \cup L(R_2), \forall R_1, R_2 \subset $
- $L(ab) = L(a) ∘ L(b)$
- L(a*) = (L(a))^* = {"", "a", "aa", "aaa", ...}
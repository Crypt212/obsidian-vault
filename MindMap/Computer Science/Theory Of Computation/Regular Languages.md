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
-  $L(ε) = {""}$
- L(a) = {"a"}  
- L(a|b) = L(a) ∪ L(b) = {"a", "b"}
- L(ab) = L(a) ∘ L(b) = {"ab"}
- L(a*) = (L(a))^* = {"", "a", "aa", "aaa", ...}
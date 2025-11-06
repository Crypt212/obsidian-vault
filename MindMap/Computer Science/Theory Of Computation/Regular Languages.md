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
- assume $\Sigma$ is an alphabet, $R_1, R_2, R_3, ..., R_n$ are regular expressions, the $L$ function has some properties:
- regular expression matches nothing: $L(\phi) = {\phi}$
- regular expression matches and empty string: $L(\varepsilon) = {\varepsilon}$
- regular expression of a symbol will match that symbol: $L(a) = {a}, \forall a \in alphabet\ \Sigma$
- union of regexs will give strings in both resulting langs: $L(R_1|R_2) = L(R_1) \cup L(R_2)$
- concatenation of regexs will give strings from $L(R_1R_2) = \{ab\ |\ a \in R_1,\ b \in R_2\}$
- $L(R^*) = (L(R))^*$
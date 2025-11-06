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
- so we call $L(R)$ a **regular language** defined by **regular expression** $R$.
- assume $\Sigma$ is an alphabet, $R_1, R_2, R_3, ..., R_n$ are regular expressions, the $L$ function has some properties:
- regular expression matches nothing: $L(\phi) = {\phi}$
- regular expression matches and empty string: $L(\varepsilon) = {\varepsilon}$
- regular expression of a symbol will match that symbol: $L(a) = {a}, \forall a \in alphabet\ \Sigma$
- union of regular expressions: $L(R_1|R_2) = L(R_1) \cup L(R_2)$
- concatenation of regular expressions: $L(R_1R_2) = \{ab\ |\ a \in R_1,\ b \in R_2\}$
- kleene star: $L(R^*) = (L(R))^*$
# Properties
## Union (∪)
If R1 and R2 are regular expressions, then R1 ∪R2 is also a regular expression.
The language described by this operation is:
L(R1 ∪ R2 ) = L(R1 ) ∪ L(R2 )
Example: If R1 = a∗ and R2 = b∗ , then R1 ∪ R2 matches strings made of
any number of a’s or b’s.
## Concatenation
If R1 and R2 are regular expressions, then R1 R2 is also a regular expression.
The concatenation of two languages is defined as:
L(R1 R2 ) = {xy | x ∈ L(R1 ), y ∈ L(R2 )}
Example: If R1 = a∗ and R2 = b∗ , then R1 R2 matches strings of a’s followed
by b’s.
## Kleene Star (\*)
If R is a regular expression, then R∗ is also a regular expression. The Kleene
star operation denotes zero or more repetitions of the language L(R):
L(R∗ ) = {ϵ} ∪ L(R) ∪ L(RR) ∪ L(RRR) ∪ · · ·
Example: If R = ab, then R∗ = (ab)∗ matches "", "ab", "abab", and so on.
## Intersection (∩)
Regular expressions are closed under intersection. If L1 and L2 are regular
languages, then:
L1 ∩ L2
is also a regular language.
## Complement (ň)
If L is a regular language, then the complement L is also regular:
L(R) = Σ∗ \ L(R)
## Diﬀerence (-)
The diﬀerence of two regular languages is also regular:
L1 − L2 = L1 ∩ L2
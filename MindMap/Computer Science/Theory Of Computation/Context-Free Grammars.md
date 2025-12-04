**Context-Free Grammar**: These are a type of formal grammars used to define context-free languages.
These grammars are instrumental in the field of computer science, particularly in the design of **programming languages** and **compilers**.
# Formalizing
- A **Context-Free Grammar** can be defined using a 4-tuple: $G = (V, \Sigma, R, S)$, where:
	- **V** is a finite set of **variables** that are used by **production rules** as placeholders for patterns of strings.
	- $\Sigma$ is a finite set of **alphabet** (terminals) used to make up the actual content of the language (aka, used to construct strings).
	- **R** is a finite set of **production rules**, where each rule is a mapping from a **variable** to a string containing **variables** and **terminals**.
	- **S** is the starting variable, and it belongs the the set of variables **V**.
## Example
- Consider the following **CFG** $G = (V, \Sigma, R, S)$:
- Variables: $V = \{S, A\}$
- Terminals: $\Sigma = \{a, b\}$
- Production Rules:
$$ S \rightarrow aAb $$
$$ A \rightarrow aA\ |\ b $$
- Start Symbol: S
- we can construct a string like this:
	- using first rule:
$$ S \rightarrow aAb $$
	- using second rule:
$$ aAb \rightarrow aaAbb $$
	- using second rule:
$$ aaAbb \rightarrow aa\ \epsilon\ bb \rightarrow aabb$$
# Properties
## Union (∪)
If $R_1$ and $R_2$ are [[regular expressions]], then $R_1 \cup R_2$ is also a [[Regular Expressions|regular expression]].
Example: If $R_1 = a∗$ and $R_2 = b∗$ , then $R_1 \cup R_2$ matches strings made of
any number of a’s or b’s.
## Concatenation
If $R_1$ and $R_2$ are [[regular expressions]], then $R_1 R_2$ is also a [[Regular Expressions|regular expression]].
Example: If $R_1 = a∗$ and $R_2 = b∗$ , then $R_1 R_2$ matches strings of a’s followed
by b’s.
## Kleene Star (\*)
If $R$ is a [[Regular Expressions|regular expression]], then $R∗$ is also a [[Regular Expressions|regular expression]].
Example: If $R = ab$, then $R∗ = (ab)∗$ matches "", "ab", "abab", and so on.
## Intersection (∩)
[[Regular Expressions]] are closed under intersection. If $L_1$ and $L_2$ are regular
languages, then:
$L_1 \cap L_2$
is also a regular language.
## Complement (ň)
If $L$ is a regular language, then the complement $L$ is also regular:
$L(R) = \Sigma∗\ -\ L(R)$
## Diﬀerence (-)
The diﬀerence of two regular languages is also regular:
$L1 − L2 = L1 \cap L2$
# Regular

# Applications of Regular Languages
- Lexical Analysis: Token recognition in compilers.
- Text Searching: Pattern matching using tools like grep or regex.
- Protocol Design: Describing simple communication patterns.
- Automated Verification: Model checking of finite-state systems.
**Context-Free Grammar**: These are a type of formal grammars used to define context-free languages.
These grammars are instrumental in the field of computer science, particularly in the design of **programming languages** and **compilers**.
# Formalization
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
$$ aAb \rightarrow aaAb $$
	- using second rule:
$$ aaAb \rightarrow aa\ \epsilon\ b \rightarrow aab$$
- so the resulting string "aab" is in the language.
# Properties
- CFGs can describe a wide variety of languages, including many programming languages and natural languages.
- They are less powerful than unrestricted grammars but more powerful than regular grammars.
- The languages defined by CFGs can be parsed using algorithms like the CYK algorithm or LL and LR parsing techniques.
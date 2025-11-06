- **Theory of Computation** is a branch of computer science and mathematics concerned with understanding the limitations of computing machines.
- **Computation** is the process of performing calculations or solving problems through a series of well-defined steps (ie, an algorithm).
# Importance of Computation theory
- **Defining limits of *Computation***: helps to avoid wasting resources (time, memory ... etc) on problems unsolvable by *Computation*.
- **Optimizing Algorithms Efficiency**: *Complexity Theory* categorizes problems based on resources needed to solve it (P, NP, NP-hard, NP-complete), providing guidance to decide whether to seek exact solutions or focus on approximations.
- **Enabling Practical Software and System Designs**: *Automata Theory* is foundational in designing programming languages and compilers and allows the creation of more reliable and optimized software systems.
- **Strengthening Cryptography and Security**: Understanding the limits of computation can help in designing secure and hard-to-break encryption systems.
- **Guiding Innovation in Emerging Technologies**: Helps defining the capabilities and limitations of new emerging computational models (like quantum computing), allowing us to design new algorithms that leverage these computational models, pushing the boundaries of what is possible.
# Definitions
- **Alphabet**: is a set of symbols. In *Automata Theory*, it represents the set of inputs.
- **String**: a finite concatenation of elements from the **Alphabet**. In *Automata Theory*, it represents the sequence of inputs.
- **Grammar**: a set of production rules that define how strings in a language are formed.
- **[[Languages|Language]]**: is the set of all strings constructed over an alphabet under the rules of a grammar.
- [[Pumping Lemmas|pumping lemma]]: fundamental tools in **theory of computation** used prove that a language does not belong to specific language classes.
- **Turing Machine**: an abstract mathematical model of computation that manipulates symbols on infinite tape according to a set of rules.
- **Decidability**: whether a problem can be solved using a turing machine that will halt and provide a correct answer for all inputs.
# Example
- - **Context-Free Grammar for balanced parentheses:**
	- Alphabet: Σ = { `(`, `)` }
	- Variables: { `S` }
	- Start Symbol: `S`
	- Production Rules (Grammar):
		1. `S -> ( S )` (A balanced thing can be inside parentheses)
		2. `S -> S S` (Two balanced things in a row are balanced)
		3. `S -> ε` (An empty string is balanced)
	- Using these rules, you can generate `"()(())"` by starting with `S` and applying the rules.
	- L = { "", (), ()(), ()(()()), }
# Finite Representation of Language
- Refers to the method of depicting a language (infinite set of strings) in a compact and precise way with finite structure.
- **WHY?** Because, while languages can be infinite set of strings, we need to describe or recognize the the language using finite mechanisms, like automata or grammars.
- There are common ways of representing languages finitely:
	- [[Regular Languages|Regular Expressions]]
	- [[Finite Automata]]
	- [[Context-Free Grammars (CFG)|Context-Free Grammars]]
	- [[Turing Machines]]
- A **Pushdown Automaton (PDA)** is a computational model that extends [[finite automata]] by including a stack as an additional storage mechanism.
- This extra memory allows PDAs to recognize a broader class of languages, specifically the class of [[Context-Free Grammars|context-free languages (CFLs)]].
# Formalization
- A **Pushdown Automaton** is a 6-tuple $P = (Q, \Sigma, \Gamma, \delta, q_0 , F )$, where:
- $Q$ is a finite set of states.
- $\Sigma$ is the input alphabet (finite set of input symbols).
- $\Gamma$ is the stack alphabet (finite set of stack symbols).
- $δ$ is the transition function, defined as: $\delta : Q × (\Sigma \cup {\epsilon}) × (\Gamma \cup {\epsilon}) → P(Q × \Gamma∗ )$. It specifies the transitions based on the current state, input symbol, and top of the stack.
- $q_0 \in Q$ is the initial state.
- $F \subseteq Q$ is the set of accepting states.
# Explanation
- The PDA operates similarly to a finite automaton, but with an additional stack data structure, which allows it to store and retrieve symbols in a Last-In-First-Out (LIFO) manner. This stack enables the PDA to handle nested structures, such as matching parentheses or palindromes, which finite automata alone cannot recognize.
- During computation, the PDA reads input symbols from the input tape, transitions between states, and pushes or pops symbols from the stack depending on the transition rules.
# Formal Description
- Each transition of a PDA depends on three things:
	- The current state of the PDA.
	- The input symbol being read (or ϵ for an empty input transition).
	- The top symbol of the stack (or ϵ for an empty stack transition).
- Given this information, the PDA moves to a new state, and the stack may be modified by pushing or popping symbols. The stack operations allow the PDA to recognize languages that require memory beyond what finite automata can manage.
## Acceptance
A PDA can accept a string in two ways:
- By final state: The PDA accepts if it reaches an accepting state after reading the entire input.
- By empty stack: The PDA accepts if the input is fully read and the stack is empty,  regardless of the current state.
# Example
- Consider a PDA that recognizes the language $L = \{a_n b_n | n \geq 0\}$, which consists of strings with an equal number of ’a’s followed by ’b’s.
- States: $Q = {q_0 , q_1 , q_2 }$
- Input alphabet: $\Sigma = \{a, b\}$
- Stack alphabet: $\Gamma = \{A, Z_0\}$, where $Z_0$ is the initial stack symbol.
- Transitions:
$δ(q_0 , a, A^nZ_0 ) = (q_0 , A^{n+1}Z_0), \forall n \geq 0$
$δ(q_0 , b, A^nZ_0 ) = (q_1 , A^{n-1}Z_0), \forall n \gt 0$
$δ(q_1 , b, A^nZ_0 ) = (q_1 , A^{n-1}Z_0), \forall n \gt 0$
$δ(q_1 , \epsilon, Z_0 ) = (q_2 , Z_0)$
- Start state: $q_0$
- Accepting state: $q_2$
This PDA works as follows:
• In state q0 , for every ’a’ encountered, the PDA pushes an ’A’ onto the
stack.
• When the first ’b’ is encountered, the PDA switches to state q1 and starts popping ’A’s from the stack for every ’b’ read.
• When all ’A’s are popped, the PDA checks if the input is fully processed and if the stack is empty, transitioning to the accepting state q2 .
Thus, the PDA accepts strings like aabb, aaabbb, but rejects strings like abb or aabbb, since they don’t have matching numbers of ’a’s and ’b’s.
# Applications
Pushdown Automata are commonly used in the following areas:
- Parsing in compilers for programming languages, especially for parsing context-free grammars.
- Recognition of context-free languages such as balanced parentheses or palindromes.
- Describing the behavior of recursive algorithms and nested structures.
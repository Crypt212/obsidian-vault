- A **Pushdown Automaton (PDA)** is a computational model that extends
[[finite automata]] by including a stack as an additional storage mechanism.
This extra memory allows PDAs to recognize a broader class of languages,
specifically the class of [[conetx|context-free languages (CFLs)]].
Definition
A Pushdown Automaton is a 6-tuple P = (Q, Σ, Γ, δ, q0 , F ), where:
• Q is a finite set of states.
• Σ is the input alphabet (finite set of input symbols).
• Γ is the stack alphabet (finite set of stack symbols).
• δ is the transition function, defined as:
δ : Q × (Σ ∪ {ϵ}) × (Γ ∪ {ϵ}) → P(Q × Γ∗ )
It specifies the transitions based on the current state, input symbol,
and top of the stack.
• q0 ∈ Q is the initial state.
• F ⊆ Q is the set of accepting states.
Explanation
The PDA operates similarly to a finite automaton, but with an additional
stack data structure, which allows it to store and retrieve symbols in a
Last-In-First-Out (LIFO) manner. This stack enables the PDA to handle
nested structures, such as matching parentheses or palindromes, which finite
automata alone cannot recognize.
121122
6. PUSHDOWN AUTOMATA (PDA)
During computation, the PDA reads input symbols from the input tape,
transitions between states, and pushes or pops symbols from the stack de-
pending on the transition rules.
Formal Description
Each transition of a PDA depends on three things:
• The current state of the PDA.
• The input symbol being read (or ϵ for an empty input transition).
• The top symbol of the stack (or ϵ for an empty stack transition).
Given this information, the PDA moves to a new state, and the stack
may be modified by pushing or popping symbols. The stack operations
allow the PDA to recognize languages that require memory beyond what
finite automata can manage.
Acceptance
A PDA can accept a string in two ways:
• By final state: The PDA accepts if it reaches an accepting state after
reading the entire input.
• By empty stack: The PDA accepts if the input is fully read and the
stack is empty, regardless of the current state.
Example
Consider a PDA that recognizes the language L = {an bn | n ≥ 0}, which
consists of strings with an equal number of ’a’s followed by ’b’s.
• States: Q = {q0 , q1 , q2 }
• Input alphabet: Σ = {a, b}
• Stack alphabet: Γ = {A, Z0 }, where Z0 is the initial stack symbol.
• Transitions:
δ(q0 , a, Z0 ) = (q0 , AZ0 )
δ(q0 , a, A) = (q0 , AA)
δ(q0 , b, A) = (q1 , ϵ)
δ(q1 , b, A) = (q1 , ϵ)
δ(q1 , ϵ, Z0 ) = (q2 , Z0 )
• Start state: q0
• Accepting state: q26.1. EXAMPLES OF PUSHDOWN AUTOMATA (PDA)
123
Explanation of Example
This PDA works as follows:
• In state q0 , for every ’a’ encountered, the PDA pushes an ’A’ onto the
stack.
• When the first ’b’ is encountered, the PDA switches to state q1 and
starts popping ’A’s from the stack for every ’b’ read.
• When all ’A’s are popped, the PDA checks if the input is fully pro-
cessed and if the stack is empty, transitioning to the accepting state
q2 .
Thus, the PDA accepts strings like aabb, aaabbb, but rejects strings like
abb or aabbb, since they don’t have matching numbers of ’a’s and ’b’s.
Applications
Pushdown Automata are commonly used in the following areas:
• Parsing in compilers for programming languages, especially for pars-
ing context-free grammars.
• Recognition of context-free languages such as balanced parentheses or
palindromes.
• Describing the behavior of recursive algorithms and nested structures.
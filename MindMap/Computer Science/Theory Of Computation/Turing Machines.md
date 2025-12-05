- A **Turing Machine (TM)** is a theoretical computational model that was introduced by Alan Turing in 1936.
- It is one of the most powerful models of computation and can simulate any algorithm.
- Turing Machines can recognize the class of languages known as recursively enumerable languages.
# Formal Definition
- A **Turing Machine** is a 7-tuple $M = (Q, \Sigma, \Gamma, \delta, q_0 , q_{accept} , q_{reject})$, where:
• Q is a finite set of states.
• $\Sigma$ is the input alphabet, which does not include the blank symbol ⊔.
• $\Gamma$ is the tape alphabet, where Σ ⊆ Γ and ⊔ ∈ Γ is the blank symbol.
• δ : Q × Γ → Q × Γ × {L, R} is the transition function, which specifies
the machine’s movement.
• q0 ∈ Q is the initial state.
• qaccept ∈ Q is the accepting state.
• qreject ∈ Q is the rejecting state, where qreject ̸= qaccept .
Components of a Turing Machine
The Turing Machine consists of three primary components:
129130
7. INTRODUCTION TO TURING MACHINES
• Tape: An infinite tape divided into cells, each capable of holding a
symbol from the tape alphabet Γ. The tape serves as both input and
unlimited memory.
• Head: The machine has a head that can read and write symbols on
the tape and move either left (L) or right (R) on the tape.
• State Register: This holds the current state of the Turing Machine,
which is one of the states from Q.
Operation of a Turing Machine
The machine operates as follows:
• The machine begins in the initial state q0 and starts reading the input
on the tape, which is written from left to right, and the rest of the
tape is blank.
• Based on the current state and the symbol under the tape head, the
machine follows the transition function δ to update its state, write a
symbol on the tape, and move the tape head either left or right.
• The computation continues until the machine reaches either the ac-
cepting state qaccept or the rejecting state qreject .
Formal Definition of the Transition Function
The transition function δ can be formally defined as:
δ : Q × Γ → Q × Γ × {L, R}
For each pair of current state and tape symbol, the transition function pro-
vides:
• The next state.
• The symbol to be written on the tape.
• The direction to move the head (left or right).
Example
Consider a Turing Machine that recognizes the language L = {w ∈ {0, 1}∗ |
w contains an equal number of 0’s and 1’s}.
• States: Q = {q0 , q1 , qaccept , qreject }
• Input alphabet: Σ = {0, 1}7.2. TURING MACHINE EXAMPLES
131
• Tape alphabet: Γ = {0, 1, X, ⊔}, where X is a symbol used for
marking.
• Transitions:
δ(q0 , 0) = (q1 , X, R)
δ(q1 , 1) = (q0 , X, L)
• Start state: q0
• Accepting state: qaccept
• Rejecting state: qreject
This Turing Machine operates as follows:
• It replaces the first unmarked 0 with an X and then searches to the
right for an unmarked 1, replacing it with X.
• The machine repeats this process until all 0’s and 1’s are marked.
• If it finds the input contains an equal number of 0’s and 1’s, it reaches
the accepting state; otherwise, it moves to the rejecting state.
Applications of Turing Machines
Turing Machines are a powerful model of computation and are used to for-
malize the concept of what it means for a function to be computable. Some
common applications include:
• Algorithm Design: Turing Machines help in analyzing the compu-
tational complexity of algorithms.
• Language Recognition: TMs recognize context-sensitive languages
and can simulate other simpler automata like finite automata and
pushdown automata.
• Decidability: Turing Machines are used to study the limits of what
problems can and cannot be solved by a computer.
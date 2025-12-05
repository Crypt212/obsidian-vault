- A **Turing Machine (TM)** is a theoretical computational model that was introduced by Alan Turing in 1936.
- It is one of the most powerful models of computation and can simulate any algorithm.
- Turing Machines can recognize the class of languages known as recursively enumerable languages.
# Formal Definition
- A **Turing Machine** is a 7-tuple $M = (Q, \Sigma, \Gamma, \delta, q_0 , q_{accept} , q_{reject})$, where:
	- $Q$ is a finite set of states.
	- $\Sigma$ is the input alphabet, which does not include the blank symbol ⊔.
	- $\Gamma$ is the tape alphabet, where $\Sigma \subseteq \Gamma$ and $⊔ \in \Gamma$ is the blank symbol.
	- $\delta : Q × \Gamma → Q × \Gamma × \{L, R\}$ is the transition function, which specifies the machine’s movement.
	- $q_0 \in Q$ is the initial state.
	- $q_{accept} \in Q$ is the accepting state.
	- $q_{reject} \in Q$ is the rejecting state, where $q_{reject} \not= q_{accept}$.
## Components of a Turing Machine
The Turing Machine consists of three primary components:
- **Tape**: An infinite tape divided into cells, each capable of holding a symbol from the tape alphabet $\Gamma$. The tape serves as both input and unlimited memory.
- **Head**: The machine has a head that can read and write symbols on the tape and move either left ($L$) or right ($R$) on the tape.
- **State Register**: This holds the current state of the Turing Machine, which is one of the states from $Q$.
## Operation of a Turing Machine
The machine operates as follows:
- The machine begins in the initial state $q_0$ and starts reading the input on the tape, which is written from left to right, and the rest of the tape is blank.
- Based on the current state and the symbol under the tape head, the machine follows the transition function $\delta$ to update its state, write a symbol on the tape, and move the tape head either left or right.
- The computation continues until the machine reaches either the accepting state $q_{accept}$ or the rejecting state $q_{reject}$.
## Formal Definition of the Transition Function
The transition function $\delta$ can be formally defined as:
$\delta : Q × \Gamma → Q × \Gamma × \{L, R\}$
For each pair of current state and tape symbol, the transition function provides:
- The next state.
- The symbol to be written on the tape.
- The direction to move the head (left or right).
## Example
Consider a **Turing Machine** that recognizes the language $L = \{w\ \in\ {0, 1}∗\ |\ w\ contains\ an\ equal\ number\ of\ 0’s\ and\ 1’s\}$.
- States: $Q = \{q_0 , q_1 , q_{accept} , q_{reject} \}$
- Input alphabet: $\Sigma = \{0, 1\}$.
- Tape alphabet: $\Gamma = \{0, 1, X, ⊔\}$, where $X$ is a symbol used for
marking.
- Transitions:
$\delta(q_0 , 0) = (q_1 , X, R)$
$\delta(q_1 , 1) = (q_0 , X, L)$
- Start state: $q_0$
- Accepting state: $q_{accept}$
- Rejecting state: $q_{reject}$
This Turing Machine operates as follows:
- It replaces the first unmarked 0 with an X and then searches to the right for an unmarked 1, replacing it with X.
- The machine repeats this process until all 0’s and 1’s are marked.
- If it finds the input contains an equal number of 0’s and 1’s, it reaches the accepting state; otherwise, it moves to the rejecting state.
# Applications of Turing Machines
Turing Machines are a powerful model of computation and are used to formalize the concept of what it means for a function to be computable. Some common applications include:
- **Algorithm Design**: **Turing Machines** help in analyzing the computational complexity of algorithms.
- **Language Recognition**: TMs recognize context-sensitive languages and can simulate other simpler automata like [[finite automata]] and [[pushdown automata]].
- **Decidability**: **Turing Machines** are used to study the limits of what problems can and cannot be solved by a computer.
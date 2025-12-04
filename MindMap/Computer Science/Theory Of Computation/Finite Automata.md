- **Finite automata (FA)** are one of the most fundamental computational models used in the study of [[languages|formal languages]] and automata theory. They are used to recognize and classify patterns within input data, and are essential for understanding [[regular languages]].
- Finite automata operate on strings of symbols from a given alphabet and decide whether the input string belongs to a particular language.
- Finite automata are characterized by a finite number of states, and they make state transitions based on input symbols.
- There are two types of Finite Automata:-
	- Deterministic Finite Automate (DFA)
	- Non-deterministic Finite Automate (NFA)
- Both DFA and NFA recognize the same class of languages, known as the [[regular languages]].
# Formalization
- A Finite Automata is defined as a 5-tuple: $M = (Q, \Sigma, \delta, q_0, F)$, where:
	- $Q$ is the set of states
	- $\Sigma$ is a finite input alphabet.
	- $\delta: Q \times \Sigma \rightarrow Q$ is a transition function; a mapping that defines what is the new state $q_{new} \in Q$ resulting from current state $q_{current} \in Q$ with an input $a \in \Sigma$ applied to it (ex, $\delta(q_1, A) = q_3, A \in \Sigma$).
	- $q_0$ is the starting state.
	- $F \subseteq Q$ is the set of accepting (final) states.
- This is also the definition of a DFA.
- NFA is the same with small difference: 
	- $\delta: (Q \cup \epsilon) \times \Sigma \rightarrow 2^Q$ is a transition function; except that:
		- it can take empty string $\epsilon$ as input.
		- it outputs a **set of states**, meaning that on some states, one output could transition to any state of that output set (that's why it is called non-deterministic)
- Although NFA could be more flexible and convenient, both NFA and DFA recognize the same class of languages: [[Regular Languages]].
- A fundamental result in automata theory states that for every NFA, there exists an equivalent DFA that recognizes the same language.
# Powerset/Subset Construction
- The process of converting an NFA into an equivalent DFA is known as the **subset construction** or **powerset construction**.
- Given: An NFA: $N = (Q, \Sigma, \delta, q_0 , F)$, where
	- $Q$ = finite set of NFA states
	- $\Sigma$ = input alphabet
	- $δ$ = transition function, $\delta : Q \times \Sigma \rightarrow 2^Q$
	- $q_0$ = start state
	- $F$ = set of accepting (final) states
- Construct: An equivalent DFA $D = (Q^`, \Sigma^`, \delta^`, q_0^`, F^`)$, where
	- $Q^`$ = $2^Q$ (set of all subsets of $Q$)
	- $q_0^′$ = $\epsilon$-closure($q_0$)
	- $F^′\ =\ \{S\ \in\ Q^′\ |\ S\ \cap\ F\ \not=\ \phi\}$
## Algorithm Steps
1. Compute $\epsilon$-closure of the start state $q_0$ ; this will be the start state of the DFA.
2. For each DFA state (subset of NFA states) and for each input symbol $a \in \Sigma$:
	1. Determine all states reachable from any state in the subset on input a.
	2. Compute $\epsilon$-closure() of all these reachable states.
	3. The resulting set forms a new DFA state.
3. Repeat Step 2 until no new states are produced.
4. Mark as final states all DFA states that contain at least one NFA final state.

> $\epsilon$-closure of a state in NFA is the set containing this state and the states it can reach using the $\epsilon$ input.
# Example
Given NFA: $N = (Q, \Sigma, \delta, q_0, F)$, where $Q = \{q_0 , q_1 , q_2\}$, Σ = {0, 1}, $q_0$ = start state, $F = \{q_2\}$
### Transition table:

| State | Input = 0      | Input = 1 |
| ----- | -------------- | --------- |
| $q_0$ | $\{q_0, q_1\}$ | $\{q_0\}$ |
| $q_1$ | $\phi$         | $\{q_2\}$ |
| $q_2$ | $\phi$         | $\phi$    |
### Construction of DFA:
- Start state: $\{q_0 \}$
- On input 0: $δ ′ (\{q_0 \}, 0) = \{q_0 , q_1 \}$
- On input 1: $δ ′ (\{q_0 \}, 1) = \{q_0 \}$
- From $\{q_0 , q_1 \}$:
	- On 0: $\{q_0 , q_1 \}$
	- On 1: $\{q_0 , q_2 \}$
- From $\{q_0 , q_2 \}$:
	- On 0: $\{q_0 , q_1 \}$
	- On 1: $\{q_0 \}$
### DFA Transition Table:

| DFA State      | Input = 0      | Input = 1      | Final State? |
| -------------- | -------------- | -------------- | ------------ |
| $\{q_0\}$      | $\{q_0, q_1\}$ | $\{q_0\}$      | No           |
| $\{q_0, q_1\}$ | $\{q_0, q_1\}$ | $\{q_0, q_2\}$ | No           |
| $\{q_0, q_2\}$ | $\{q_0, q_1\}$ | $\{q_0, q_2\}$ | Yes          |
### Final States: $F = \{\{ q_0, q_2 \}\}$
# Thompsons Construction Algorithm
- A systematic method for inducing a NFA from a [[Regular Expressions|regular expression]], the resulting NFA accepts exactly the same language as described by [[Regular Expressions|regular expression]].
- It is a fundamental feature of lexical analysis and compiler design; where regular expressions are transformed into finite automata for token recognition.
## How it works
- Each [[Regular Expressions|regular expression]] operation (concatenation, union, Kleene star) corresponds to a small NFA fragment with a single starting state and ending state.
- Those fragments are combined together using $\epsilon$-transitions.
## Building Blocks
- **Single Symbol**:
- **Concatenation**:
- **Union**:
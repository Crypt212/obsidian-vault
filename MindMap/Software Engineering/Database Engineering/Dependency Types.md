# Terminology

| **Determinant**         | The attribute or set of attributes on the left side of a functional dependency. It determines the values of the attributes on the right side.                                                   |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Dependent Attribute** | The attribute or set of attributes on the right side of a functional dependency that is determined by the determinant.                                                                          |
| **Closure**             | The set of all attributes that can be functionally determined by a given set of attributes X. Denoted as X+. If the closure X+ resolves to all attributes in a relation, then X is a ***key***. |

# Functional Dependency ($X\ \rightarrow\ Y$)

>All functional dependencies are considered multi-valued dependencies (but you know, with one value), and all rules applicable to multi-valued dependencies are applicable to functional dependencies.

- **Trivial Functional Dependency**: Y is *a subset* of X.
- **Partial Functional Dependency**: *A part* of X *uniquely determines* Y.
- **Full Functional Dependency**: *The entirety* of X *uniquely determines* Y.
- **Transitive Functional Dependency**: $X\ \rightarrow\ Y,\ Y\ \rightarrow\ Z$ in the same relation.
## Rules

### Splitting Rule
- This:   $A \rightarrow B_1,\ B_2,\ B_3,\ ...,\ B_n$
- Gives this:   $A \rightarrow B_1,\ A\ \rightarrow\ B_2,\ A\ \rightarrow\ B_3,\ ...,\ A\ \rightarrow\ B_n$

- But this:   $A_1,\ A_2,\ A_3,\ ...,\ A_n\ \rightarrow\ B$
- Does ***Not*** give this:   $A_1\ \rightarrow B,\ A_2\ \rightarrow\ B,\ A_3\ \rightarrow\ B,\ ...,\ A_n\ \rightarrow\ B$
### Combining Rule
- Basically the inverse of **Splitting Rule**.

- This:  $A \rightarrow B_1,\ A\ \rightarrow\ B_2,\ A\ \rightarrow\ B_3,\ ...,\ A\ \rightarrow\ B_n$
- Gives this:   $A \rightarrow B_1,\ B_2,\ B_3,\ ...,\ B_n$
### Trivial-dependency Rule
- If $A\ \rightarrow\ B$ is a trivial dependency, then $A\ \rightarrow\ A\ \cup\ B$ and $A\ \rightarrow\ A\ \cap\ B$.
### Transitive Rule
- If $A\ \rightarrow\ B$ and $B\ \rightarrow\ C$ then $A\ \rightarrow\ C$.
# Multi-valued Dependency ($X\ \twoheadrightarrow\ Y$)

>X determines Y but with Y having more than one value for one value of X.

- **Trivial Multi-valued Dependency**: Y is a subset of X.
- **Non-Trivial Multi-valued Dependency**: Y is not subset of X. :)
## Rules

### Intersection Rule
- If $A\ \twoheadrightarrow\ B$ and $A\ \twoheadrightarrow\ C$, then $A\ \twoheadrightarrow\ B\ \cap\ C$.
### Transitive Rule
- If $A\ \twoheadrightarrow\ B$ and $B\ \twoheadrightarrow\ C$, then $A\ \twoheadrightarrow\ B\ -\ C$.


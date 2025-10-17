- Formal mathematical language for describing database relationships and design.

# Concepts

| **Schema** | Structural description of the relation, describing its attributes architecture, attribute domains, constraints, ... etc. |
| ---------- | ------------------------------------------------------------------------------------------------------------------------ |
# Schema

- Schema is represented in this form: $$relation\_name(attr_1, attr_2, ..., attr_n)$$
- Relations could be produced by other relation expressions.
# Relational Operators

## Select ($\sigma_{condition}$)

- Select only tuples satisfying the condition. Example:
$$ Schema: Students (sid, age, hobby) $$
$$ \sigma_{age > 12}\ Students $$
> This is will select only students with `age > 12`.
## Project ($\pi_{set\ of\ attributes}$)

- Pick only specified attributes. Example:
$$ Schema: Students (sid, age, hobby) $$
$$ \pi_{sid, age}\ Students $$
>This will produce the instance of this relation with only `sid` and `age` attributes of this tables.
## Joins

- **Cross-Product ($R_1 \times R_2$)**: Combine relations, allows duplicate attributes, for example if R<sub>1</sub> has age and R<sub>2</sub> has age, results in relation that has two age attributes with every combination.
- **Natural-Join ($R_1 \bowtie R_2$)**: Combine relations by matching common attributes, if there are no matching attributes, the result is empty relationship since there is no matches. It is 
equivalent to this expression:
$$R_1 \bowtie R_2 = \pi_{schema(R_1)\ \cup\ schema(R_2)}(\sigma_{R_1(a_1) =\ R_2(a_1)\ \wedge\ R_1(a_2) =\ R_2(a_2)\ \wedge\ ...}(R1 \times R2))$$
$$ \forall a_n\ is\ common\ attribute\ in\ both\ relations$$
- **Theta-Join ($R_1 \bowtie_\theta R_2$)**: Also called join, is just cross join with a select condition applied to it. It is equivalent to this expression:
$$R_1 \bowtie_\theta R_2 = \sigma_\theta (R1 \times R2)$$
## Set Operations

- Operands of these operations must have the same schema.

- **Union ($R_1\ \cup\ R_2$)**: Combines all records of both relations.
- **Difference ($R_1\ \cap\ R_2$)**: Has records existing both relations.
- **Difference ($R_1 - R_2$)**: Has records from first relation but not in second one.
## Rename

- $P_{R(A_1,\ A_2,\ ...,\ A_n)}(E)$: Renames columns to (A1, A2, ..., An) and relation name to R.
- $P_{A_1,\ A_2,\ ...,\ A_n}(E)$: Renames just columns to (A1, A2, ..., An).
- $P_{R}(E)$: Renames just relation name to R.


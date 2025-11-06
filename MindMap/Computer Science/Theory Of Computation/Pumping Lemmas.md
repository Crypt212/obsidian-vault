- a **Pumping [[Lemma]]** fundamental tools in **theory of computation** used prove that a language does not belong to specific language classes.
- these [[lemma|lemmas]] provide a property that all languages of specific class must satisfy.
- if the language in test does not satisfy then it is proven to not be of that class.
# Term Analogy (Why "pumping")
- pumping comes from the fact that we are defining some part in the string in a language that could be pumped (repeated in the same place) with the newly generated string still being in the language.
# Pumping Lemma for [[Regular Languages]]
- Let $L$ be a regular language. Then there exists an integer $p \gt 0$ (called the **pumping length**) such that every string $w \in L$ with $|w| \geq p$ can be divided into three parts:
$$w = xyz$$
- satisfying the following conditions:
	1. $|y| > 0$
	2. $|xy| ≤ p$
	3. $xy^i z ∈ L, \forall i ≥ 0$
- **Intuition**: 
	- a property of any [[regular languages|regular language]] is that any string in that language has some section that can be *pumped* (repeated) to generate new string that also is in the language.
	- the lemma is used to prove a language is not [[Regular Languages|regular]] by finding a string in it that doesn't have any part that could be repeated to generate a string 
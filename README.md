[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/wM4-KOzy)
# Little-o

In addition to the big-O, big-$\Omega$, and big-$\Theta$ notation that
we covered at the beginning of this class, a few other notations are sometimes
used in asymptotic analysis.  For example, "little-$o$" notation.

Prove (i.e.\ give a formal mathematical proof) that $f(n)\in o(g(n))$ implies
that $f(n)\in O(g(n))$.

Hint: The proof will be *very* short and *very* easy. You can start by
identifying the differences between the definitions of O and o.

I have started with the formal definition of $o$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

// Credit to ChatGPT for teaching me proof notation

Little o formal definition:
$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$

Big O formal definiton:
$f(n)\in O(g(n)) \iff \exists c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$

Claim: prove that if $f(n)\in o(g(n))$, then $f(n)\in O(g(n))$

1. Assume the first statement, $f(n)\in o(g(n))$, is true.
    This implies that for any positive constant $C$, there exists a constant $n_0$,
    such that $\forall n\ge n_0$, $f(n) < Cg(n)$

2. Since we want to prove $f(n)\in O(g(n))$, we must define constants $C'$ and $n_0'$.
    We will define them with the same values, i.e. $C=C'$ and $n_0=n_0'$

3. Since $f(n)\in o(g(n))$, then $f(n) < Cg(n)$ for all $n\ge n_0$, it logically
    follows that $f(n) < C'g(n)$ for all $n\ge n_0'$

4. Therefore, by the formal definition of $O$, if $f(n)\in o(g(n))$, then $f(n)\in O(g(n))$
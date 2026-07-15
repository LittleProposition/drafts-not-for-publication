# Exponentially Many Hamiltonian Subsets from the Crux

[Read the manuscript (PDF)](./exponentially-many-hamiltonian-subsets-from-the-crux.pdf)

## Overview

A vertex set $A\subseteq V(G)$ is called a **Hamiltonian subset** if the
induced subgraph $G[A]$ contains a Hamiltonian cycle. Let $h(G)$ denote the
number of Hamiltonian subsets of a graph $G$.

For $0<\alpha<1$, the $\alpha$-**crux** of $G$ is defined by

$$
c_\alpha(G)
=
\min\{
|V(H)|:
H\subseteq G
\text{ and }
\overline d(H)\ge \alpha\overline d(G)
\}.
$$

Thus, $c_\alpha(G)$ measures the minimum number of vertices required to retain
an $\alpha$-fraction of the average degree of $G$.

Cambie, Gao and Liu proved that if $G$ is an $n$-vertex graph of sufficiently
large average degree and

$$
t=c_{1/5}(G),
$$

then

$$
h(G)\ge \frac{n}{B}2^{\beta t/\log^{16}t}.
$$

for absolute constants $B,\beta>0$. They asked whether the factor
$\log^{16}t$ in the exponent is necessary.

This manuscript answers that question negatively.

## Main result

We prove that there are absolute constants $\kappa,c,d_0>0$ such that every
$n$-vertex graph $G$ with average degree at least $d_0$ satisfies

$$
h(G)\ge \kappa n2^{ct},
\qquad
t=c_{1/5}(G).
$$

In particular, the exponent can be taken to be linear in the crux parameter
$t$, up to an absolute constant. This removes the polylogarithmic loss from
the previous lower bound.

Equivalently, every graph of sufficiently large average degree contains
exponentially many induced subgraphs with Hamiltonian cycles, where the
exponential rate is controlled by the size of its $1/5$-crux.

## Relation to previous work

The problem belongs to the study of Hamiltonian subsets initiated by
Komlós's conjecture. Komlós conjectured that, among graphs of minimum degree
at least $d$, the complete graph $K_{d+1}$ minimizes the number of
Hamiltonian subsets. This conjecture was proved for sufficiently large $d$
by Kim, Liu, Sharifzadeh and Staden.

Cambie, Gao and Liu later studied lower bounds in terms of average degree and
the crux parameter. Their argument gave an exponential lower bound with a
$\log^{16}t$ loss in the exponent. The present manuscript shows that this
loss is not intrinsic.

## Main ingredients

The proof retains the global counting framework of Cambie, Gao and Liu but
replaces its rooted counting input.

The main new ingredient is a random-restriction counting lemma. Let $H$ be
a graph and let

$$
s=c_{9/10}(H).
$$

By choosing induced subgraphs obtained from random vertex restrictions, one
finds many restrictions whose average degree remains close to that of $H$.
Each such restriction still has large crux. A long-cycle theorem of
Haslegrave, Hu, Kim, Liu, Luan and Wang then gives a cycle of length
$\Omega(s)$ in every good restriction.

A double-counting argument shows that these restrictions produce

$$
2^{\Omega(s)}
$$

distinct Hamiltonian subsets. Averaging vertex--subset incidences then gives
a vertex contained in exponentially many of them.

The proof separates two regimes.

### Moderately sized expanders

When the extracted sublinear expander $H$ has order at most
$2^{\eta t}$, the random-restriction argument gives a vertex contained in
$2^{\Omega(t)}$ Hamiltonian subsets.

### Very large expanders

When $|V(H)|>2^{\eta t}$, the wheel construction of Cambie, Gao and Liu
already contains sufficiently many independently selectable paths. It
therefore produces $2^{\Omega(t)}$ Hamiltonian subsets through a common
vertex.

These two cases give a rooted exponential bound. A minimal-counterexample
argument then turns the rooted statement into the global lower bound
$\kappa n2^{ct}$.

## Additional features

The random-restriction lemma does not require expansion.

A bipartite version of the rooted bound is also proved: the common vertex can
be required to lie in either prescribed side of a fixed bipartition. This
side-specific form is used in the global counting argument.

## Keywords and related search terms

Hamiltonian subsets; Hamiltonian vertex sets; induced Hamiltonian subgraphs;
induced subgraphs containing Hamiltonian cycles; counting Hamiltonian
subsets; many Hamiltonian cycles; graphs of large average degree; crux of a
graph; $c_\alpha(G)$; Hamiltonian subsets and the crux; exponential lower
bound for Hamiltonian subsets; removal of a polylogarithmic loss; Cambie,
Gao and Liu; Komlós conjecture on Hamiltonian subsets; sublinear expanders;
long cycles in graphs; random vertex restrictions; random induced
subgraphs; double counting; wheel construction; extremal graph theory.

## Status

This is a preliminary and unrefereed manuscript. It is posted here to make
the result publicly accessible to researchers interested in Hamiltonian
subsets, graph crux parameters, long cycles, and related extremal graph
theory problems. The manuscript may be revised or developed further, and a
later version may eventually be submitted for publication.

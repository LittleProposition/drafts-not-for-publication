[README_biased_pentagonal_cut.md](https://github.com/user-attachments/files/30147819/README_biased_pentagonal_cut.md)
# A Biased Pentagonal Cut and the Bound $\delta_c\le 0.78876$

[Read the manuscript (PDF)](./a-biased-pentagonal-cut-and-the-bound-delta-c-at-most-0.78876.pdf)

## Overview

For a graph $G$, let $t(G)$ denote the maximum number of edges in a
triangle-free subgraph of $G$, and let $b(G)$ denote the maximum number of
edges in a bipartite subgraph of $G$.

Erdős asked when these two extremal quantities must be equal. Balogh,
Keevash and Sudakov introduced the asymptotic minimum-degree threshold
$\delta_c$ for this problem: informally, $\delta_c$ is the least constant
such that every sufficiently large $n$-vertex graph $G$ with

$$
\delta(G)\ge (\delta_c+o(1))n
$$

satisfies

$$
t(G)=b(G).
$$

They proved

$$
\frac34\le \delta_c<0.791
$$

and conjectured that

$$
\delta_c=\frac34.
$$

This manuscript improves the known upper bound.

## Main result

We prove that, for all sufficiently large $n$, every $n$-vertex graph $G$
with

$$
\delta(G)\ge \frac{19719}{25000}n
$$

satisfies

$$
t(G)=b(G).
$$

Consequently,

$$
\delta_c\le \frac{19719}{25000}=0.78876.
$$

Thus the previous upper bound $\delta_c<0.791$ of Balogh, Keevash and
Sudakov can be lowered to $0.78876$.

## Relation to previous work

The proof follows the deletion-and-structure framework developed by Balogh,
Keevash and Sudakov.

Starting from a maximum triangle-free subgraph, one repeatedly deletes
vertices of low degree. The remaining triangle-free core is then analysed
using Jin's structural theorem for triangle-free graphs of large minimum
degree, together with weighted estimates from the work of Balogh, Keevash
and Sudakov.

Because the surviving core has minimum degree above $5/14$ of its order,
only four structural types can occur:

- a bipartite type;
- a $C_5$-type;
- an $F_3$-type;
- an $F_4$-type,

where $F_j$ denotes the $j$th Andrásfai graph.

The bipartite, $F_3$, and $F_4$ cases are excluded using the existing
arguments and estimates. The improvement comes entirely from a sharper
analysis of the $C_5$-type case.

## The biased pentagonal cut

Suppose the relevant core is partitioned cyclically into five classes

$$
V_0,V_1,V_2,V_3,V_4.
$$

Balogh, Keevash and Sudakov used a symmetric random cut adapted to this
pentagonal structure. Here it is replaced by a biased cyclic random cut.

After choosing a uniformly random cyclic shift, vertices are placed on one
side independently with probabilities

$$
\left(
0,\,
1,\,
0,\,
\frac{18347}{25000},\,
\frac{18347}{25000}
\right).
$$

Averaging over the five cyclic shifts gives the following separation
probabilities for pairs of vertices:

$$
\pi_0=\frac{122062591}{781250000},
\qquad
\pi_1=\frac{1205737591}{1562500000},
\qquad
\pi_2=\frac25,
$$

according to whether the two vertices lie in the same class, in adjacent
classes, or in classes at cyclic distance two.

This asymmetric choice changes the objective function in the completion
linear program for the $C_5$-type core and yields the improved constant
$19719/25000$.

## Proof outline

The proof has four main components.

### 1. Deletion process

Let $H$ be a maximum-edge triangle-free subgraph of the ambient graph.
Vertices of low degree are deleted until a dense triangle-free core
$\Gamma$ remains.

A deletion inequality relates the edge density of $\Gamma$ to the original
triangle-free density.

### 2. Structural classification

Jin's theorem and the structural estimates of Balogh, Keevash and Sudakov
reduce the possible core structures to the bipartite, $C_5$, $F_3$, and
$F_4$ cases.

The bipartite case is ruled out by the original tangency argument, while the
$F_3$ and $F_4$ cases are excluded by direct density comparisons.

### 3. Completion linear program

In the $C_5$ case, the edges inside the core, outside the core, and across
the cut satisfy minimum-degree and capacity constraints.

The biased pentagonal cut is applied inside the core, while outside vertices
are placed independently and uniformly. The remaining optimization is a
small linear program, whose minimizer can be written explicitly.

### 4. Exact univariate verification

After the structural reductions and linear-program calculation, the final
inequalities reduce to sign conditions for several univariate rational
functions on the rational interval

$$
\left[
\frac{13469}{37500},
\frac{36633}{100000}
\right].
$$

After clearing denominators, the relevant numerator polynomials have degrees

$$
3,\ 2,\ 3,\ 4,\ 8.
$$

Their signs are certified by exact Sturm root counts. The manuscript
contains the complete verification code, written in Python with SymPy and
using exact rational arithmetic throughout.

The code checks:

- the feasible range of the $C_5$ parameter;
- the lower bound $u(g)\ge 3/5$;
- concavity of the final quadratic in the core-size parameter;
- positivity at both endpoints of the feasible interval;
- the exact numerical margins in the $F_3$ and $F_4$ cases.

## Computer-assisted component

The only computer-assisted part is the exact algebraic verification of five
sign conditions for univariate rational functions.

No floating-point computation is used. The program reconstructs all
quantities directly from the formulas in the manuscript and performs exact
Sturm root counts over rational intervals. The full source code and expected
output are included in the paper, so the verification is reproducible from a
single LaTeX file.

## Keywords

Triangle-free subgraphs; bipartite subgraphs; maximum cut; minimum-degree
threshold; Erdős problem; Balogh--Keevash--Sudakov; Jin's theorem;
Andrásfai graphs; $C_5$-homomorphic triangle-free graphs; biased random cut;
pentagonal cut; exact Sturm theorem verification; extremal graph theory.

## Status

This is a preliminary and unrefereed manuscript. It is posted here so that
researchers interested in the Erdős problem on largest triangle-free and
bipartite subgraphs, the threshold $\delta_c$, and the Balogh--Keevash--
Sudakov framework can find and examine the result.

The manuscript may be revised or developed further, and a later version may
eventually be submitted for publication.

Comments, corrections, and reports of possible errors are welcome through
GitHub Issues.

## AI assistance

The initial idea and much of the proof strategy were suggested by an AI system. The author independently checked and verified all mathematical claims, calculations, and arguments in the manuscript.

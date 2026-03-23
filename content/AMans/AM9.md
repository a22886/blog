+++
date = '2026-03-11T13:58:37+08:00'
title = "9. Discrete Valuation Rings and Dedekind Domains"
categories = ["交换代数"]
series = ["Solutions to Atiyah-MacDonald Commutative Algebra"]
+++

You may want to see [this](../am0/) for unclear notations.

---

{{<exercise 1>}}
Let $A$ be a Dedekind domain, $S$ a multiplicatively closed subset of $A$. Show that $S^{-1}A$ is either a Dedekind domain or the field of fractions of $A$.
QUESTIONANDANSWERSTRING\
Dedekind rings are the one-dimensional integrally closed Noetherian domains, and taking localization preserves all but the dimension property, which must decrease by the ideal correspondence. If the dimension is still $1$ then it is a Dedekind domain, and if the dimension is $0$ then the localization is a field; it is a subfield of $\operatorname{Frac}(A)$ containing $A$, so it must be $\operatorname{Frac}(A)$ itself.
TOMANDJERRYSTRINGLITERAL\
Suppose that $S\neq A-\{0\}$, and let $H$, $H'$ be the ideal class groups of $A$ and $S^{-1}A$ respectively. Show that extension of ideals induces a surjective homomorphism $H\to H'$.
QUESTIONANDANSWERSTRING\
The extension of fractional ideals $\mathfrak{a}\mapsto S^{-1}\mathfrak{a}$ induces a homomorphism on the group of non-zero fractional ideals $I(A)\to I(S^{-1}A)$. The fractional ideals of a Noetherian ring is of the form $x^{-1}\mathfrak{a}$ where $x\in A-\{0\}$ and $\mathfrak{a}$ is an ideal of $A$, hence it is clear that this homomorphism is surjective, and maps principal fractional ideals to principal fractional ideals, so it induces a surjective homomorphism $H\to H'$.
{{</exercise>}}

{{<exercise 2>}}
Let $A$ be a Dedekind domain. If $f=a_0+a_1x+\cdots+a_nx^n$ is a polynomial with coefficients in $A$, the *content* of $f$ is the ideal $c(f)=(a_0,\ldots,a_n)$ in $A$. Prove *Gauss's lemma* that $c(fg)=c(f)c(g)$.\
[Localize at each maximal ideal.]
QUESTIONANDANSWERSTRING\
Two ideals coincide if and only if they coincide when localized at each maximal ideal, hence we assume $A$ is already localized to a discrete valuation ring, and here every ideal is principal. Let $c(f)=(a)$, $c(g)=(b)$, then $c(f/a)=(1)$ and $c(g/b)=(1)$, so $c(fg/ab)=(1)$ by Chapter 1, Exercise 2 iv), hence $c(fg)=(ab)=c(f)c(g)$.
{{</exercise>}}

{{<exercise 3>}}
A valuation ring (other than a field) is Noetherian if and only if it is a discrete valuation ring.
QUESTIONANDANSWERSTRING\
We only need to prove the 'only if' direction; let the Noetherian valuation ring be $A$. Notice that $A$$ is a local domain, while Chapter 5, Exercise 28 tells us its ideals is totally ordered with respect to $\subseteq$. Every ideal of $A$ is finitely generated, and ordering its generators by $\subseteq$ on the principal ideals they generate shows that every ideal of $A$ is principal.\
Now every fractional ideal of $A$ is of the form $x^{-1}(y)$, hence having inverse $y^{-1}(x)$; Proposition 9.7 tells us that $A$ is a discrete valuation ring {{<explain>}}The condition that $A$ is not a field is used in Proposition 9.7, where $\Sigma$ in its proof would be empty if $A$ is a field.{{</explain>}}.
{{</exercise>}}

{{<exercise 4>}}
Let $A$ be a local domain which is not a field and in which the maximal ideal $\mathfrak{m}$ is principal and $\bigcap_{n=1}^{\infty}\mathfrak{m}^n=0$. Prove that $A$ is a discrete valuation ring.
QUESTIONANDANSWERSTRING\
For any $x\in A$ we can find the maximum $t\ge0$ such that $x\in\mathfrak{m}^t$. Then $x=up^t$ where $\mathfrak{m}=(p)$, and $u$ is a unit. It is easy to verify that $v(x)=t$ is a valuation on $A$ which naturally extends to $\operatorname{Frac}(A)$ making $A$ a discrete valuation ring.
{{</exercise>}}

{{<exercise 5>}}
Let $M$ be a finitely-generated module over a Dedekind domain. Prove that $M$ is flat $\Leftrightarrow M$ is torsion-free.\
[Use Chapter 3, Exercise 13 and Chapter 7, Exercise 16.]
QUESTIONANDANSWERSTRING\
The properties are all local properties, hence we may localize and assume $A$ is a discrete valuation ring, which is a principal ideal domain, on which the structure theorem gives that torsion-free are free. Chapter 7, Exercise 16 tells us tht flat is locally free, hence the result.
{{</exercise>}}

{{<exercise 6>}}
Let $M$ be a finitely-generated torsion module ($T(M)=M$) over a Dedekind domain $A$. Prove that $M$ is uniquely representable as a finite direct sum of modules $A/\mathfrak{p}_i^{n_i}$, where $\mathfrak{p}_i$ are non-zero prime ideals of $A$. [For each $\mathfrak{p}\neq0$, $M_\mathfrak{p}$ is a torsion $A_\mathfrak{p}$-module; use the structure theorem for modules over a principal ideal domain.]
QUESTIONANDANSWERSTRING\
Combining the natural homomorphisms we have a $u:M\to\bigoplus_\mathfrak{p}M_\mathfrak{p}$. Notice that by structure theorem for PID (hence for DVR) each $M_\mathfrak{p}$ is of the form $\bigoplus A_\mathfrak{p}/(\mathfrak{p}A_\mathfrak{p})^{n_i}\simeq\bigoplus A/\mathfrak{p}^{n_i}$. Also those $\mathfrak{p}$ such that $M_\mathfrak{p}\neq0$ form the set $\operatorname{Supp}(M)=V(\operatorname{Ann}(M))$, which is finite due to the prime power decomposition of $\operatorname{Ann}(M)$, hence the direct sum is finite.\
It suffices to prove that $u$ is an isomorphism; as $(M_\mathfrak{p})_\mathfrak{q}=0$ for any two distinct prime ideals, hence $u$ is an isomorphism at any localization, hence it is an isomorphism {{<explain>}}Proposition 3.9{{</explain>}}.
{{</exercise>}}

{{<exercise 7>}}
Let $A$ be a Dedekind domain and $\mathfrak{a}\neq0$ an ideal in $A$. Show that every ideal in $A/\mathfrak{a}$ is principal.
QUESTIONANDANSWERSTRING\
For the prime power decomposition $\mathfrak{a}=\prod\mathfrak{p}_i^{n_i}$, we have $A/\mathfrak{a}\simeq\prod A/\mathfrak{p}_i^{n_i}\simeq\prod A_{\mathfrak{p}_i}/(\mathfrak{p}_iA_{\mathfrak{p}_i})^{n_i}$, each factor in the right is a quotient of a PID, hence the left is also PID.
TOMANDJERRYSTRINGLITERAL\
Deduce that every ideal in $A$ can be generated by at most 2 elements.
QUESTIONANDANSWERSTRING\
Obvious by the claim before.
{{</exercise>}}

{{<exercise 8>}}
Let $\mathfrak{a},\mathfrak{b},\mathfrak{c}$ be three ideals in a Dedekind domain. Prove that \[\mathfrak{a}\cap(\mathfrak{b}+\mathfrak{c})=(\mathfrak{a}\cap \mathfrak{b})+(\mathfrak{a}\cap \mathfrak{c})\] \[\mathfrak{a}+(\mathfrak{b}\cap \mathfrak{c})=(\mathfrak{a}+\mathfrak{b})\cap(\mathfrak{a}+\mathfrak{c})\] [Localize.]
QUESTIONANDANSWERSTRING\
We may only verify these at any localization, but after localizing we get a DVR, whose lattice of nonzero ideals is isomorphic to $\mathbf{Z}_{\ge0}$, hence the result.
{{</exercise>}}

{{<exercise 9>}}
(Chinese Remainder Theorem). Let $\mathfrak{a}_1,\ldots,\mathfrak{a}_n$ be ideals and let $x_1,\ldots,x_n$ be elements in a Dedekind domain $A$. Then the system of congruences $x\equiv x_i\pmod{\mathfrak{a}_i}(1\le i\le n)$ has a solution $x$ in $A\Leftrightarrow x_i\equiv x_j\pmod{\mathfrak{a}_i+\mathfrak{a}_j}$ whenever $i\neq j$.\
[This is equivalent to saying that the sequence of $A$-module \[A\xrightarrow{\phi}\bigoplus_{i=1}^nA/\mathfrak{a}_i\xrightarrow{\psi}\bigoplus_{i< j}A/(\mathfrak{a}_i+\mathfrak{a}_j)\] is exact, where $\phi$ and $\psi$ are defined as follows:\
$\phi(x)=(x+\mathfrak{a}_1,\ldots,x+\mathfrak{a}_n)$; $\psi(x_1+\mathfrak{a}_1,\ldots,x_n+\mathfrak{a}_n$ has $(i,j)$-component $x_i-x_j+\mathfrak{a}_i+\mathfrak{a}_j$. To show that this sequence is exact it is enough to show that it is exact when localized at any $\mathfrak{p}\neq 0$: in other words we may assume that $A$ is a discrete valuation ring, and then it is easy.] {{<explain>}}The hint is exactly the answer.{{</explain>}}
{{</exercise>}}

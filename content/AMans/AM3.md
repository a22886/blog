+++
date = '2026-02-02T16:44:10+08:00'
title = "3. Rings and Modules of Fractions"
categories = ["交换代数"]
series = ["Solutions to Atiyah-MacDonald Commutative Algebra"]
+++

You may want to see [this](../am0/) for unclear notations.

---

{{<exercise 1>}}
Let $S$ be a multiplicatively closed subset of a ring $A$, and let $M$ be a finitely generated $A$-module. Prove that $S^{-1}M$ if and only if there exists $s\in S$ such that $sM=0$.
QUESTIONANDANSWERSTRING\
$S^{-1}M=0$ is saying that every $(m,s')$ is equivalent to $(0,1)$ by construction, which means all $m\in M$ is annihilated by some $s\in S$. Notice that $M$ is finitely generated, so this is then equivalent to having one $s\in S$ that annihilates every $m\in M$ (take product of the $s_i$ that annihilates the generators.)
{{</exercise>}}

{{<exercise 2>}}
Let $\mathfrak{a}$ be an ideal of a ring $A$, and let $S=1+\mathfrak{a}$. Show that $S^{-1}\mathfrak{a}$ is contained in the Jacobson radical of $S^{-1}A$.
QUESTIONANDANSWERSTRING\
For every $a/s\in S^{-1}\mathfrak{a}$ and $b/s'\in S^{-1}A$ we have \[(1-\frac as\frac b{s'})^{-1}=\frac{ss'}{ss'-ab}\in S^{-1}A\] because $ss'-ab\equiv 1\bmod \mathfrak{a}$. The conclusion follows by Proposition 1.9.
TOMANDJERRYSTRINGLITERAL\
Use this result and Nakayama's lemma to give a proof of (2.5) which does not depend on determinants. [If $M=\mathfrak{a}M$, then $S^{-1}M=(S^{-1}\mathfrak{a})(S^{-1}M)$, hence by Nakayama we have $S^{-1}M=0$. Now use Exercise 1.] {{<explain>}}The hint is exactly the answer.{{</explain>}}
{{</exercise>}}

{{<exercise 3>}}
Let $A$ be a ring, let $S$ and $T$ be two multiplicatively closed subsets of $A$, and let $U$ be the image of $T$ in $S^{-1}A$. Show that the rings $(TS)^{-1}A$ and $U^{-1}(S^{-1}A)$ are isomorphic.
QUESTIONANDANSWERSTRING\
The underlying sets are both $T\times S\times B/\sim$, where the equivalence relation are both \[(t_1,s_1,b_1)\sim(t_2,s_2,b_2)\Leftrightarrow \exists s_3\in S,t_3\in T,f(s_3t_3)(b_1f(s_2t_2)-b_2f(s_1t_1))=0\] and the operation are obviously also the same.
{{</exercise>}}

{{<exercise 4>}}
Let $f:A\to B$ be a homomorphism of rings and let $S$ be a multiplicatively closed subset of $A$. Let $T=f(S)$. Show that $S^{-1}B$ and $T^{-1}B$ are isomorphic as $S^{-1}A$ modules.
QUESTIONANDANSWERSTRING\
The action of $S$ on $B$ is exactly the multiplication of $T$ on $B$. We only need to verify the obvious ring isomorphism is compatible with $S^{-1}A$ action, which is also obvious.
{{</exercise>}}

{{<exercise 5>}}
Let $A$ be a ring. Suppose that, for each prime ideal $\mathfrak{p}$, the local ring $A_\mathfrak{p}$ has no nilpotent element $\neq0$. Show that $A$ has no nilpotent element $\neq0$.
QUESTIONANDANSWERSTRING\
By Corollary 3.12 we have $\mathfrak{N}_{A_\mathfrak{p}}=(\mathfrak{N}_A)_{\mathfrak{p}}$, hence Proposition 3.8 gives the result.
TOMANDJERRYSTRINGLITERAL\
If each $A_\mathfrak{p}$ is an integral domain, is $A$ necessarily an integral domain?
QUESTIONANDANSWERSTRING\
No. Consider $A=\mathbf{Q}^2$, with prime ideals being $\mathbf{Q}\times 0$ and $0\times\mathbf{Q}$. The corresponding localized rings are both $\mathbf{Q}$, which is integral, but $A$ itself is not.
{{</exercise>}}

{{<exercise 6>}}
Let $A$ be a ring $\neq0$ and let $\Sigma$ be the set of all multiplicatively closed subsets $S$ of $A$ such that $0\not\in S$. Show that $\Sigma$ has maximal elements, and that $S\in \Sigma$ is maximal if and only if $A-S$ is a minimal prime ideal of $A$.
QUESTIONANDANSWERSTRING\
The existence of maximal elements is  direct application of Zorn's lemma. For any $S\in \Sigma$ there is a prime ideal $\mathfrak{p}$ not intersecting $S$: this is because $A_S\neq0$ and we can take the contraction of its prime ideal. But this shows $S\subseteq A-\mathfrak{p}\in \Sigma$, which obviously proves the result.
{{</exercise>}}

{{<exercise 7>}}
A multiplicatively closed subset $S$ of a ring $A$ is said to be *saturated* if \[xy\in S\Leftrightarrow x\in S\text{ and }y\in S\] Prove that
TOMANDJERRYSTRINGLITERAL\
i) $S$ is saturated $\Leftrightarrow A-S$ is a union of prime ideals.
QUESTIONANDANSWERSTRING\
$\Leftarrow$ is trivial. For $\Rightarrow$, we shall only prove that for every $x\in A-S$ there is a prime ideal $\mathfrak{p}\ni x$ not intersecting $S$. We can take $\mathfrak{p}$ to be the maximal element (whose existence is guaranteed by Zorn's lemma) of the set \[\{\text{ideal }\mathfrak{a}\ni x:\mathfrak{a}\cap S=\varnothing\}\]
TOMANDJERRYSTRINGLITERAL\
ii) If $S$ is any multiplicatively closed subset of $A$, there is a unique smallest saturated multiplicatively closed subset $\overline{S}$ containing $S$, and that $\overline{S}$ is the complement in $A$ of the union of the prime ideals which do not meet $S$. ($\overline{S}$ is called the *saturation* of $S$.)\
If $S=1+\mathfrak{a}$, where $\mathfrak{a}$ is an ideal of $A$, find $\overline{S}$.
QUESTIONANDANSWERSTRING\
The saturation is exactly as given. The saturation of $S=1+\mathfrak{a}$ also can be written as \[\overline{S}=A-\bigcup_{\text{maximal }\mathfrak{m}\supseteq\mathfrak{a}}\mathfrak{m}\]
{{</exercise>}}

{{<exercise 8>}}
Let $S$, $T$ be multiplicatively closed subsets of $A$, such that $S\subseteq T$. Let $\phi:S^{-1}A\to T^{-1}A$ be the homomorphism which maps each $a/x\in S^{-1}A$ to $a/s$ considered as an element of $T^{-1}A$. Show that the following statements are equivalent:\
i) $\phi$ is bijective.\
ii) For each $t\in T$, $t/1$ is a unit in $S^{-1}A$.\
iii) For each $t\in T$ there exists $x\in A$ such that $xt\in S$.\
iv) $T$ is contained in the saturation of $S$ (Exercise 7).\
v) Every prime ideal which meets $T$ also meets $S$.
QUESTIONANDANSWERSTRING\
It is clear that i) $\Leftrightarrow$ ii) $\Leftrightarrow$ iii) $\Rightarrow$ v) $\Leftrightarrow$ iv). Now we prove iv) $\Rightarrow$ iii): if not, we take $t\in T\subseteq \overline{S}$ such that $(t)\cap S=\varnothing$, then there is a prime ideal containing $t$ not intersecting $S$ {{<explain>}}See solution of Exercise 7, i){{</explain>}}, which contradicts the expression of $\overline{S}$ given in Exercise 7, ii).
{{</exercise>}}

{{<exercise 9>}}
The set $S_0$ of all non-zero-divisors in $A$ is a saturated multiplicatively closed subset of $A$. Hence the set $D$ of zero-divisors in $A$ is a union of prime ideals (see Chapter 1, Exercise 14). Show that every minimal prime ideal of $A$ is contained in $D$. [Use Exercise 6.]
QUESTIONANDANSWERSTRING\
By Exercise 6 it suffices to prove that if $x\not\in S$ for some maximal multiplicatively closed subset $S$ not containing 0, then $x$ is a zero-divisor; this is because by maximality if we add $\{x^ns:s\in S,n\ge0\}$ into $S$ we must bring 0 into the set.
TOMANDJERRYSTRINGLITERAL\
The ring $S_0^{-1}A$ is called the *total ring of fractions* of $A$. Prove that
TOMANDJERRYSTRINGLITERAL\
i) $S_0$ is the largest multiplicatively closed subset of $A$ for which the homomorphism $A\to S_0^{-1}A$ is injective.
QUESTIONANDANSWERSTRING\
Injectivity of $A\to S^{-1}A$ is equivalent to saying if $\exists s\in S, sa=0$, then $a=0$, i.e. $S\subseteq S_0$.
TOMANDJERRYSTRINGLITERAL\
ii) Every element in $S_0^{-1}A$ is either a zero-divisor or a unit.
QUESTIONANDANSWERSTRING\
The numerator of every non-zero-divisor in $S_0^{-1}A$ cannot be a zero-divisor in $A$.
TOMANDJERRYSTRINGLITERAL\
iii) Every ring in which every non-unit is a zero-divisor is equal to its total ring of fractions (i.e., $A\to S_0^{-1}A$ is bijective).
QUESTIONANDANSWERSTRING\
The inverse is given by $S_0^{-1}A\xrightarrow{a/s\mapsto as^{-1}}A$.
{{</exercise>}}

{{<exercise 10>}}
Let $A$ be a ring.
TOMANDJERRYSTRINGLITERAL\
i) If $A$ is absolutely flat (Chapter 2, Exercise 27) and $S$ is any multiplicatively closed subset of $A$, then $S^{-1}A$ is absolutely flat.
QUESTIONANDANSWERSTRING\
The condition of 'principal ideals are idempotent' is preserved under localization.
TOMANDJERRYSTRINGLITERAL\
ii) $A$ is absolutely flat $\Leftrightarrow A_\mathfrak{m}$ is a field for each maximal ideal $\mathfrak{m}$.
QUESTIONANDANSWERSTRING\
$\Rightarrow$ is because absolutely flat local rings are fields by Chapter 2, Exercise 28. $\Leftarrow$ is because modules on a field must be flat, then by Proposition 3.10 we know every $A$-module is flat.
{{</exercise>}}

{{<exercise 11>}}
Let $A$ be a ring. Prove that the following are equivalent:\
i) $A/\mathfrak{N}$ is absolutely flat ($\mathfrak{N}$ being the nilradical of $A$).\
ii) Every prime ideal of $A$ is maximal.\
iii) $\operatorname{Spec}(A)$ is a $T_1$ space (i.e., every subset consisting of a single point is closed).\
iv) $\operatorname{Spec}(A)$ is Hausdorff.
QUESTIONANDANSWERSTRING\
It is clear that ii) $\Rightarrow$ iv) $\Rightarrow$ iii), and by Chapter 1, Exercise 18 we have iii) $\Rightarrow$ ii).\
By Exercise 10, ii) we know that $A$ being absolutely flat is equivalent to saying that for every prime ideal $\mathfrak{p}$, $(A/\mathfrak{N})_\mathfrak{p}\simeq A_\mathfrak{p}/\mathfrak{N}_{A_\mathfrak{p}}$ is a field, which is equivalent to saying $A_\mathfrak{p}$ only have one prime ideal, i.e. (by Proposition 3.11) there are no prime ideals of $A$ containing another prime ideal, which is obviously equivalent to iii).
TOMANDJERRYSTRINGLITERAL\
If these conditions are satisfied, show that $\operatorname{Spec}(A)$ is compact and totally disconnected (i.e., the only connected subsets of $\operatorname{Spec}(A)$ are those consisting of a single point).
QUESTIONANDANSWERSTRING\
For any set $S$ containing two prime ideals $\mathfrak{p}\neq\mathfrak{q}$ take $x\in\mathfrak{p}\backslash\mathfrak{q}$, by absolute flatness there is some $(e)=(x)$ with $e$ idempotent, so that $V((e))$ and $V((1-e))$ is a partition of the *whole* space separating $\mathfrak{p}$ and $\mathfrak{q}$, therefore $S$ is not connected.
{{</exercise>}}

{{<exercise 12>}}
Let $A$ be an integral domain and $M$ an $A$-module. An element $x\in M$ is a *torsion element* of $M$ if $\operatorname{Ann}(x)\neq0$, that is if $x$ is killed by some non-zero element of $A$. Show that the torsion elements of $M$ form a submodule of $M$ {{<explain>}}Obvious.{{</explain>}}. This submodule is called the *torsion submodule* of $M$ and is denoted by $T(M)$. If $T(M)=0$, the module $M$ is said to be torsion-free. Show that
TOMANDJERRYSTRINGLITERAL\
i) If $M$ is any $A$-module, then $M/T(M)$ is torsion-free.
QUESTIONANDANSWERSTRING\
Obvious.
TOMANDJERRYSTRINGLITERAL\
ii) If$f:M\to N$ is a module homomorphism, then $f(T(M))\subseteq T(N)$.
QUESTIONANDANSWERSTRING\
Also obvious.
TOMANDJERRYSTRINGLITERAL\
iii) If $0\to M'\to M\to M''\to0$ is an exact sequence, then the sequence $0\to T(M')\to T(M)\to T(M'')$ is exact.
QUESTIONANDANSWERSTRING\
$T(M')=T(M)\cap M'=\ker[T(M)\to T(M'')]$.
TOMANDJERRYSTRINGLITERAL\
iv) If $M$ is any $A$-module, then $T(M)$ is the kernel of the mapping $x\mapsto 1\otimes x$ of $M$ into $K\otimes_A M$, where $K$ is the field of fractions of $A$.
QUESTIONANDANSWERSTRING\
Let $S=A\backslash\{0\}$, then the mentioned map is the canonical $M\to S^{-1}M$, whose kernel are those annihilated by some $s\in S$, i.e. $T(M)$.
TOMANDJERRYSTRINGLITERAL\
[For iv), show that $K$ may be regarded as the direct limit of its submodules $A\xi(\xi\in K)$; using Chapter 1, Exercise 15 and Exercise 20,, show that if $1\otimes x=0$ in $K\otimes_A M$ then $1\otimes x=0$ in $A\xi\otimes_A M$ for some $\xi\neq0$. Deduce that $\xi^{-1}x=0$.]
{{</exercise>}}

{{<exercise 13>}}
Let $S$ be a multiplicatively close subset of an integral domain $A$. In the notation of Exercise 12, show that $T(S^{-1}M)=S^{-1}(TM)$.
QUESTIONANDANSWERSTRING\
$m/s\in T(S^{-1}M)\Leftrightarrow \exists s', s'm=0\Leftrightarrow m\in T(M)\Leftrightarrow m/s\in S^{-1}T(M)$.
TOMANDJERRYSTRINGLITERAL\
Deduce that the following are equivalent:\
i) $M$ is torsion-free.\
ii) $M_\mathfrak{p}$ is torsion-free for all prime ideals $\mathfrak{p}$.\
iii) $M_{\mathfrak{m}}$ is torsion-free for all maximal ideal $\mathfrak{m}$.
QUESTIONANDANSWERSTRING\
Proposition 3.8 says that 'is zero' is a local property, while torsion-free is saying torsion 'is zero', and taking torsion commutes with localization.
{{</exercise>}}

{{<exercise 14>}}
Let $M$ be an $A$-module and $\mathfrak{a}$ an ideal of $A$. Suppose that $M_\mathfrak{m}=0$ for all maximal ideals $\mathfrak{m}\supseteq\mathfrak{a}$. Prove that $M=\mathfrak{a}M$. [Pass to the $A/\mathfrak{a}$-module $M/\mathfrak{a}M$ and use (3.8).] {{<explain>}}The hint is exactly the answer.{{</explain>}}
{{</exercise>}}

{{<exercise 15>}}
Let $A$ be a ring, and let $F$ be the $A$-module $A^n$. Show that every set of $n$ generators of $F$ is a basis of $F$. [Let $x_1,\ldots,x_n$ be a set of generators and $e_1,\ldots,e_n$ the canonical basis of $F$. Define $\phi:F\to F$ by $\phi(e_i)=x_i$. Then $\phi$ is surjective and we have to prove that it is an isomorphism. By (3.9) we may assume that $A$ is a local ring. Let $N$ be the kernel of $\phi$ and let $k=A/\mathfrak{m}$ be the residue field of $A$. Since $F$ is a flat $A$-module, the exact sequence $0\to N\to F\to F\to 0$ gives an exact sequence $0\to k\otimes N\to k\otimes F\xrightarrow{1\otimes\phi}k\otimes F\to 0$. Now $k\otimes F=k^n$ is an $n$-dimensional vector space over $k$; $1\otimes \phi$ is surjective, hence bijective, hence $k\otimes N=0$.\
Also $N$ is finitely generated, by Chapter 2, Exercise 12, hence $N=0$ by Nakayama's lemma. Hence $\phi$ is an isomorphism.]
TOMANDJERRYSTRINGLITERAL\
Deduce that every set of generators of $F$ has at least $n$ elements.
QUESTIONANDANSWERSTRING\
Otherwise carefully completing it to be a set of $n$ generators makes some of its elements linearly dependent.
{{</exercise>}}

{{<exercise 16>}}
Let $B$ be a flat $A$-algebra. Then the following conditions are equivalent:\
i) $\mathfrak{a}^{ec}=\mathfrak{a}$ for all ideals $\mathfrak{a}$ of $A$.\
ii) $\operatorname{Spec}(B)\to\operatorname{Spec}(A)$ is surjective.\
iii) For every maximal ideal $\mathfrak{m}$ of $A$ we have $\mathfrak{m}^e\neq(1)$.\
iv) If $M$ is any non-zero $A$-module, then $M_B\neq0$.\
v) For every $A$-module $M$, the mapping $x\mapsto1\otimes x$ of $M$ into $M_B$ is injective.\
[For i) $\Rightarrow$ ii), use (3.16). ii) $\Rightarrow$ iii) is clear.\
iii) $\Rightarrow$ iv): Let $x$ be a non-zero element of $M$ and let $M'=Ax$. Since $B$ is flat over $A$ it is enough to show that $M'_B\neq0$. We have $M'\simeq A/\mathfrak{a}$ for some ideal $\mathfrak{a}\neq(1)$, hence $M_B'\simeq B/\mathfrak{a}^e$. Now $\mathfrak{a}\subseteq \mathfrak{m}$ for some maximal ideal $\mathfrak{m}$, hence $\mathfrak{a}^e\subseteq \mathfrak{m}^e\neq(1)$. Hence $M_B'\neq0$.\
iv) $\Rightarrow$ v): Let $M'$ be the kernel of $M\to M_B$. Since $B$ is flat over $A$, the sequence $0\to M_B'\to M_B\to (M_B)_B$ is exact. But (Chapter 2, Exercise 13, with $N=M_B$) the mapping $M_B\to (M_B)_B$ is injective, hence $M_B'=0$ and therefore $M'=0$.\
v) $\Rightarrow$ i): Take $M=A/\mathfrak{a}$.]
TOMANDJERRYSTRINGLITERAL\
$B$ is said to be *faithfully flat* over $A$.
{{</exercise>}}

{{<exercise 17>}}
Let $A\xrightarrow{f}B\xrightarrow{g}C$ be ring homomorphisms. If $g\circ f$ is flat and $g$ is faithfully flat, then $g$ is flat.
QUESTIONANDANSWERSTRING\
Take injection $M\to N$ between $A$-modules, then by flatness \[\ker[C\otimes_B(B\otimes_A M)\to C\otimes_B(B\otimes_A N)]=0\] by faithful flatness the left hand side is equal to $C\otimes_B\ker[B\otimes_A M\to B\otimes_A N]$, hence by Exercise 16 iv) the second kernel is 0. Hence $B\otimes_A\bullet$ preserves injection, i.e. $B$ is flat.
{{</exercise>}}

{{<exercise 18>}}
Let $f:A\to B$ be a flat homomorphism of rings, let $\mathfrak{q}$ be a prime ideal of $B$ and let $\mathfrak{p}=\mathfrak{q}^c$. Then $f^*:\operatorname{Spec}(B_\mathfrak{q})\to\operatorname{Spec}(A_\mathfrak{p})$ is surjective.
QUESTIONANDANSWERSTRING\
Let $B_{\mathfrak{q}^c}$ be the localization of the $A$-module $B$ with respect to $A\backslash \mathfrak{q}^c$. By Proposition 3.10 it is flat on $A_{\mathfrak{q}^c}$. Notice that the only maximal ideal of $A_{\mathfrak{q}^c}$ is $\mathfrak{q}^cA_{\mathfrak{q}^c}$ whose image in $B_\mathfrak{q}$ is contained in $\mathfrak{q}B_\mathfrak{q}\neq(1)$, hence by Exercise 16 it is actually faithfully flat. However $f(A\backslash \mathfrak{q}^c)\subseteq B\backslash \mathfrak{q}$, hence $B_\mathfrak{q}$ is a localization of $B_{\mathfrak{q}^c}$, which is flat on it by Corollary 3.6. Hence by Exercise 17 we prove the result.
{{</exercise>}}

{{<exercise 19>}}
Let $A$ be a ring, $M$ an $A$-module. Th *support* of $M$ is defined to be the set $\operatorname{Supp}(M)$ of prime ideals $\mathfrak{p}$ of $A$ such that $M_\mathfrak{p}\neq0$. Prove the following results:
TOMANDJERRYSTRINGLITERAL\
i) $M\neq0\Leftrightarrow\operatorname{Supp}(M)\neq\varnothing$.
QUESTIONANDANSWERSTRING\
Consider the maximal ideal $\mathfrak{m}$ containing $\operatorname{Ann}(M)$, and by Exercise 1 $M_\mathfrak{m}\neq0$.
TOMANDJERRYSTRINGLITERAL\
ii) $V(\mathfrak{a})=\operatorname{Supp}(A/\mathfrak{a})$.
QUESTIONANDANSWERSTRING\
By Exercise 1, $\mathfrak{p}\in\operatorname{Supp}(A/\mathfrak{a})\Leftrightarrow A\backslash\mathfrak{p}\cap \operatorname{Ann}(A/\mathfrak{a})=\varnothing\Leftrightarrow \mathfrak{p}\supseteq\mathfrak{a}$.
TOMANDJERRYSTRINGLITERAL\
iii) If $0\to M'\to M\to M''\to0$ is an exact sequence, then $\operatorname{Supp}(M)=\operatorname{Supp}(M')\cup\operatorname{Supp}(M'')$.
QUESTIONANDANSWERSTRING\
By Proposition 3.3 for prime ideal $\mathfrak{p}$ there is an exact sequence $0\to M_\mathfrak{p}'\to M_\mathfrak{p}\to M_\mathfrak{p}''\to0$, from which it is obvious.
TOMANDJERRYSTRINGLITERAL\
iv) If $M=\sum M_i$, then $\operatorname{Supp}(M)=\bigcup\operatorname{Supp}(M_i)$.
QUESTIONANDANSWERSTRING\
For prime ideal $\mathfrak{p}$ we have $M_\mathfrak{p}=\sum (M_i)\mathfrak{p}$.
TOMANDJERRYSTRINGLITERAL\
v) If $M$ is finitely generated, then $\operatorname{Supp}(M)=V(\operatorname{Ann}(M))$ (and is therefore a closed subset of $\operatorname{Spec}(A)$).
QUESTIONANDANSWERSTRING\
Proof similar to ii).
TOMANDJERRYSTRINGLITERAL\
vi) If $M$, $N$ are finitely generated, then $\operatorname{Supp}(M\otimes_A N)=\operatorname{Supp}(M)\cap\operatorname{Supp}(N)$. [Use Chapter 2, Exercise 3.]
QUESTIONANDANSWERSTRING\
For prime ideal $\mathfrak{p}$ we have $(M\otimes_AN)_\mathfrak{p}\simeq M_\mathfrak{p}\otimes_{A_\mathfrak{p}}N_\mathfrak{p}$, then it is obvious by Chapter2, Exercise 3.
TOMANDJERRYSTRINGLITERAL\
vii) If $M$ is finitely generated and $\mathfrak{a}$ is an ideal of $A$, then $\operatorname{Supp}(M/\mathfrak{a}M)=V(\mathfrak{a}+\operatorname{Ann}(M))$.
QUESTIONANDANSWERSTRING\
Apply ii), vi) to $M/\mathfrak{a}M\simeq A/\mathfrak{a}\otimes_AM$ {{<explain>}}Chapter 2, Exercise 2{{</explain>}}.
TOMANDJERRYSTRINGLITERAL\
viii) If $f:A\to B$ is a ring homomorphism and $M$ is a finitely generated $A$-module, then $\operatorname{Supp}(B\otimes_A M)={f^*}^{-1}(\operatorname{Supp}(M))$.
QUESTIONANDANSWERSTRING\
By definition $\operatorname{Ann}_B(B\otimes_AM)\supseteq\operatorname{Ann}(M)^e$, hence \[{f^*}^{-1}(\operatorname{Supp}(M))={f^*}^{-1}V(\operatorname{Ann}(M))=V(\operatorname{Ann}(M)^e)\supseteq V(\operatorname{Ann}_B(B\otimes_AM))\] with right hand side equal to $\operatorname{Supp}(B\otimes_AM)$.\
For $\mathfrak{q}\in\operatorname{Spec}(B)$ we next prove $\mathfrak{q}^c\in\operatorname{Supp}(M)\Rightarrow \mathfrak{q}\in\operatorname{Supp}(B\otimes_AM)$. This is because $M_{\mathfrak{q}^c}\neq0$ as $A_{\mathfrak{q}^c}$-module, and $(B_\mathfrak{q})_{\mathfrak{q}^c}=B_\mathfrak{q}\neq0$, hence $(B_\mathfrak{q})_{\mathfrak{q}^c}\otimes_{A_{\mathfrak{q}^c}} M_{\mathfrak{q}^c}\neq0$, i.e. $B_\mathfrak{q}\otimes_A M\neq0$. Then \[(B\otimes_A M)_\mathfrak{q}\simeq B_\mathfrak{q}\otimes_BB\otimes_AM\simeq B_\mathfrak{q}\otimes_A M\neq0\]
Hence proven, i.e. both sides of the question contains each other, so they must be equal.
{{</exercise>}}

{{<exercise 20>}}
Let $f:A\to B$ be a ring homomorphism, $f^*:\operatorname{Spec}(B)\to\operatorname{Spec}(A)$ the associated mapping. Show that
TOMANDJERRYSTRINGLITERAL\
i) Every prime ideal of $A$ is a contracted ideal $\Leftrightarrow f^*$ is surjective. 
QUESTIONANDANSWERSTRING\
Direct consequence of Proposition 3.16.
TOMANDJERRYSTRINGLITERAL\
ii) Every prime ideal of $B$ is an extended ideal $\Rightarrow f^*$ is injective.
QUESTIONANDANSWERSTRING\
If $\mathfrak{p}^c=\mathfrak{q}^c$, then by Proposition 1.17 $\mathfrak{p}=\mathfrak{p}^{ce}=\mathfrak{q}^{ce}=\mathfrak{q}$.
TOMANDJERRYSTRINGLITERAL\
Is the converse of ii) true?
QUESTIONANDANSWERSTRING\
No. We only need to make prime ideal extensions not prime anymore, e.g. consider $A\to A[x]\to A[x]/(x^2)$.
{{</exercise>}}

{{<exercise 21>}}
i) Let $A$ be a ring, $S$ a multiplicatively closed subset of $A$, and $\phi:A\to S^{-1}A$ the canonical homomorphism. Show that $\phi^*:\operatorname{Spec}(S^{-1}A)\to\operatorname{Spec}(A)$ is a homeomorphism of $\operatorname{Spec}(S^{-1}A)$ onto its image in $X=\operatorname{Spec}(A)$. Let this image be denoted by $S^{-1}X$.\
In particular, if $f\in A$, the image of $\operatorname{Spec}(A_f)$ in $X$ is the basic open set $X_f$ (Chapter 1, Exercise 17).
QUESTIONANDANSWERSTRING\
The isomorphism is solely due to the prime ideal correspondence of Proposition 3.11. The second part is because those prime ideals not intersecting $S_f$ are exactly those not containing $f$.
TOMANDJERRYSTRINGLITERAL\
ii) Let $f:A\to B$ be a ring homomorphism. Let $X=\operatorname{Spec}(A)$ and $Y=\operatorname{Spec}(B)$, and let $f^*:Y\to X$ be the mapping associated with $f$. Identifying $\operatorname{Spec}(S^{-1}A)$ with its canonical image $S^{-1}X$ in $X$, and $\operatorname{Spec}(S^{-1}B)$ ($=\operatorname{Spec}(f(S)^{-1}B)$) with its canonical image $S^{-1}Y$ in $Y$, show that $S^{-1}f^*:\operatorname{Spec}(S^{-1}B)\to\operatorname{Spec}(S^{-1}A)$ is the restriction of $f^*$ to $S^{-1}Y$, and that $S^{-1}Y={f^*}^{-1}(S^{-1}X)$.
QUESTIONANDANSWERSTRING\
For $\mathfrak{q}\in S^{-1}Y$, we have \[\frac as\in(S^{-1}f)^{-1}(S^{-1}\mathfrak{q})\Leftrightarrow \exists s_1,s_2\in S, q\in\mathfrak{q},f(s_1)(f(a)f(s_2)-f(s)q)=0\] but this is equivalent to $f(a)\in\mathfrak{q}$ as $\mathfrak{q}\cap f(S)=\varnothing$. Thus $(S^{-1}f)^*$ is the restriction of $f^*$. The second statement comes from the equivalence \[\mathfrak{q}\in S^{-1}Y\Leftrightarrow \mathfrak{q}\cap f(S)=\varnothing\Leftrightarrow S\cap f^{-1}(\mathfrak{q})=\varnothing\Leftrightarrow f^*(\mathfrak{q})\in S^{-1}X\]
TOMANDJERRYSTRINGLITERAL\
iii) Let $\mathfrak{a}$ be an ideal of $A$ and let $\mathfrak{b}=\mathfrak{a}^e$ be its extension in $B$. Let $\overline{f}:A/\mathfrak{a}\to B/\mathfrak{b}$ be the homomorphism induced by $f$. If $\operatorname{Spec}(A/\mathfrak{a})$ is identified with its canonical image $V(\mathfrak{a})$ in $X$, and $\operatorname{Spec}(B/\mathfrak{b})$ with its canonical image $V(\mathfrak{b})$ in $Y$, show that $\overline{f}^*$ is the restriction of $f^*$ to $V(\mathfrak{b})$.
QUESTIONANDANSWERSTRING\
Obvious by definition.
TOMANDJERRYSTRINGLITERAL\
iv) Let $\mathfrak{p}$ be a prime ideal of $A$. Take $S=A-\mathfrak{p}$ in ii) and then reduce $\bmod S^{-1}\mathfrak{p}$ as in iii). Deduce that the subspace ${f^*}^{-1}(\mathfrak{p})$ of $Y$ is naturally homeomorphic to $\operatorname{Spec}(B_\mathfrak{p}/\mathfrak{p}B_\mathfrak{p})=\operatorname{Spec}(k(\mathfrak{p})\otimes_A B)$, where $k(\mathfrak{p})$ is the residue field of the local ring $A_\mathfrak{p}$.
QUESTIONANDANSWERSTRING\
Taking localization restricts to those prime ideals with image contained in $\mathfrak{p}$, while taking quotient restricts to those with images containing $\mathfrak{p}$. Also $B_\mathfrak{p}/\mathfrak{p}B_\mathfrak{p}\simeq k(\mathfrak{p})\otimes_A B$ is obvious because quotient and localization 'commute' with tensor products.
TOMANDJERRYSTRINGLITERAL\
$\operatorname{Spec}(k(\mathfrak{p})\otimes_A B)$ is called the *fiber* of $f^*$ over $\mathfrak{p}$.
{{</exercise>}}

{{<exercise 22>}}
Let $A$ be a ring and $\mathfrak{p}$ a prime ideal of $A$. Then the canonical image of $\operatorname{Spec}(A_\mathfrak{p})$ in $\operatorname{Spec}(A)$ is equal to the intersection of all the open neighborhoods of $\mathfrak{p}$ in $\operatorname{Spec}(A)$.
QUESTIONANDANSWERSTRING\
They both corresponds to the set of all prime ideals contained in $\mathfrak{p}$.
{{</exercise>}}

{{<exercise 23>}}
Let $A$ be a ring, let $X=\operatorname{Spec}(A)$ and let $U$ be a basic open set in $X$ (i.e., $U=X_f$ for some $f\in A$: Chapter 1, Exercise 17).\
i) If $U=X_f$, show that the ring $A(U)=A_f$ depends only on $U$ and not on $f$.\
ii) Let $U'=X_g$ be another basic open set such that $U'\subseteq U$. Show that there is an equation of the form $g^n=uf$ for some integer $n>0$ and some $u\in A$, and use this to define a homomorphism $\rho:A(U)\to A(U')$ (i.e., $A_f\to A_g$) by mapping $a/f^m$ to $au^m/g^{mn}$. Show that $\rho$ depends only on $U$ and $U'$. This homomorphism is called the *restriction* homomorphism.\
iii) If $U=U'$, then $\rho$ is the identity map.\
iv) If $U\supseteq U'\supseteq U''$ are basic open sets in $X$, show that the diagram {{<image 180 70>}}AMimg/AM3_1.svg{{</image>}} (in which the arrows are the restriction homomorphisms) is commutative.\
v) Let $x$ ($=\mathfrak{p}$) be a point of $X$. Show that \[\varinjlim_{U\ni x}A(U)\simeq A_\mathfrak{p}\]
The assignment of the ring $A(U)$ to each basic open set $U$ of $X$, and the restriction homomorphisms $\rho$, satisfying the conditions iii) and iv) above, constitutes a *presheaf of rings* on the basis of open sets $(X_f)_{f\in A}$. v) says that the stalk of this presheaf at $x\in X$ is the corresponding local ring $A_\mathfrak{p}$. {{<explain>}}Details of Exercise 23 and Exercise 24 can be found in numerous books on algebraic geometry (e.g. GTM 52), and is omitted here.{{</explain>}}
{{</exercise>}}

{{<exercise 24>}}
Show that the presheaf of Exercise 23 has the following property. Let $(U_i)_{i\in I}$ be a covering of $X$ by basic open sets. For each $i\in I$ let $s_i\in A(U_i)$ be such that, for each pair of indices $i$, $j$, the images of $s_i$ and $s_j$ in $A(U_i\cap U_j)$ are equal. Then there exists a unique $s\in A$ ($=A(X)$) whose image in $A(U_i)$ is $s_i$, for all $i\in I$. (This essentially implies that the presheaf is a *sheaf*.) 
{{</exercise>}}

{{<exercise 25>}}
Let $f:A\to B$, $g:B\to V$ be ring homomorphisms and let $h:A\to B\otimes_A C$ be defined by $h(x)=f(x)\otimes g(x)$. Let $X$, $Y$, $Z$, $T$ be the prime spectra of $A$, $B$, $C$, $B\otimes_A C$ respectively. Then $h^*(T)=f^*Y\cap g^*(Z)$.\
[Let $\mathfrak{p}\in X$, and let $k=k(\mathfrak{p})$ be the residue field at $\mathfrak{p}$. By Exercise 21, the fiber ${h^*}^{-1}(\mathfrak{p})$ is the spectrum of $(B\otimes_A C)\otimes_A k\simeq (B\otimes_A k)\otimes_k(C\otimes_A k)$. Hence $\mathfrak{p}\in h^*(T)\Leftrightarrow (B\otimes_A k)\otimes_k(C\otimes_A k)\neq 0\Leftrightarrow B\otimes_A k\neq 0 \text{ and }C\otimes_A k\neq 0\Leftrightarrow \mathfrak{p}\in f^*(Y)\cap g^*(Z)$.] {{<explain>}}The hint is exactly the answer.{{</explain>}}
{{</exercise>}}

{{<exercise 26>}}
Let $(B_\alpha, g_{\alpha\beta})$ be a direct system of rings and $B$ the direct limit. For each $\alpha$, let $f_\alpha:A\to B_\alpha$ be a ring homomorphism such that $g_{\alpha\beta}\circ f_\alpha=f_\beta$ whenever $\alpha\le \beta$ (i.e. the $B_\alpha$ form a direct system of $A$-algebras). The $f_\alpha$ induce $f:A\to B$. Show that \[f^*(\operatorname{Spec}(B))=\bigcap_\alpha f_\alpha^*(\operatorname{Spec}(B_\alpha))\]
[Let $\mathfrak{p}\in \operatorname{Spec}(A)$. Then ${f^*}^{-1}(\mathfrak{p})$ is the spectrum of \[B\otimes_A k(\mathfrak{p})\simeq \varinjlim(B_\alpha\otimes_A k(\mathfrak{p})\] (since tensor products commute with direct limits: Chapter 2, Exercise 20). By Exercise 21 of Chapter 2 it follows that ${f^*}^{-1}(\mathfrak{p})=\varnothing$ if and only if $B_\alpha\otimes_A k(\mathfrak{p})=0$ for some $\alpha$, i.e., if and only if ${f_\alpha^*}^{-1}(\mathfrak{p})=\varnothing$.] {{<explain>}}The hint is exactly the answer.{{</explain>}}
{{</exercise>}}

{{<exercise 27>}}
i) Let $f_\alpha:A\to B_\alpha$ be any family of $A$-algebras and let $f:A\to B$ be their tensor product over $A$ (Chapter 2, Exercise 23). Then \[f^*(\operatorname{Spec}(B))=\bigcap_\alpha f_\alpha^*(\operatorname{Spec}(B_\alpha))\] [Use Examples {{<explain>}}I would say that the authors meant Exercises{{</explain>}} 25 and 26.]
QUESTIONANDANSWERSTRING\
The definition of a general tensor product is the filtered direct limit of finite tensor products, and by Exercise 25 and 26 we have the result.
TOMANDJERRYSTRINGLITERAL\
ii) Let $f_\alpha:A\to B_\alpha$ be any finite family of $A$-algebras and let $B=\prod_\alpha B_\alpha$. Define $f:A\to B$ by $f(x)=(f_\alpha(x))$. Then $f^*(\operatorname{Spec}(B))=\bigcup\limits_\alpha f_\alpha^*(\operatorname{Spec}(B_\alpha))$.
QUESTIONANDANSWERSTRING\
By Chapter 1, Exercise 22, $\operatorname{Spec}(B)$ is the disjoint union of $\operatorname{Spec}(B_\alpha)$; also $f_\alpha$ is obviously the restriction of $f$.
TOMANDJERRYSTRINGLITERAL\
iii) Hence the subsets of $X=\operatorname{Spec}(A)$ of the form $f^*(\operatorname{Spec}(B))$, where $f:A\to B$ is a ring homomorphism, satisfy the axioms for closed sets in a topological space. The associated topology is the *constructible* topology on $X$. It is finer than the Zariski topology (i.e., there are more open sets, or equivalently more closed sets).
QUESTIONANDANSWERSTRING\
It is finer because $V(\mathfrak{a})$ is the image of $\operatorname{Spec}(A/\mathfrak{a})$.
TOMANDJERRYSTRINGLITERAL\
iv) Let $X_C$ denote the set $X$ endowed with the constructible topology. Show that $X_C$ is quasi-compact.
QUESTIONANDANSWERSTRING\
Equivalently if some closed sets have empty intersection then some finitely many of them have empty intersection. This is because intersection of closed sets is given by tensor products {{<explain>}}See Exercise 27, i){{</explain>}}, which is defined as the limit of finite tensor products, which is 0 only if some finite tensor product is 0 by Chapter 2, Exercise 21.
{{</exercise>}}

{{<exercise 28>}}
(Continuation of Exercise 27.)
TOMANDJERRYSTRINGLITERAL\
i) For each $g\in A$, the set $X_g$ (Chapter 1, Exercise 17) is both open and closed in the constructible topology.
QUESTIONANDANSWERSTRING\
It is the image of $\operatorname{Spec}(A_g)$ hence closed, while its complement is $V((g))$ also closed.
TOMANDJERRYSTRINGLITERAL\
ii) Let $C'$ denote the smallest topology on $X$ for which the sets $X_g$ are both open and closed, and let $X_{C'}$ denote the set $X$ endowed with this topology. Show that $X_{C'}$ is Hausdorff.
QUESTIONANDANSWERSTRING\
For any two points $\mathfrak{p}\neq\mathfrak{q}$ take arbitrary $g\in\mathfrak{p}\Delta\mathfrak{q}$ {{<explain>}}symmetric difference{{</explain>}}, then open sets $X_g$ and its complement separates those points.
TOMANDJERRYSTRINGLITERAL\
iii) Deduce that the identity mapping $X_C\to X_{C'}$ is a homeomorphism. Hence a subset $E$ of $X$ is of the form $f^*(\operatorname{Spec}(B))$ for some $f:A\to B$ if and only if it is closed in the topology $C'$.
QUESTIONANDANSWERSTRING\
A continuous bijection from a compact space to a Hausdorff space is a homeomorphism.
TOMANDJERRYSTRINGLITERAL\
The topological space $X_C$ is compact, Hausdorff and totally disconnected.
QUESTIONANDANSWERSTRING\
We still need to prove that it's totally disconnected; that's because the partition in ii) is a partition of the whole space.
{{</exercise>}}

{{<exercise 29>}}
Let $f:A\to B$ be a ring homomorphism. Show that $f^*:\operatorname{Spec}(B)\to\operatorname{Spec}(A)$ is a continuous *closed* mapping (i.e., maps closed sets to closed sets) for the constructible topology.
QUESTIONANDANSWERSTRING\
By definition it is closed; we only need to prove continuity, i.e. the inverse images of closed sets are closed. For closed set $g^*(\operatorname{Spec}(C))$ with $g:A\to C$, define $u:B\to B\otimes_AC, x\mapsto x\otimes1$, thus $uf$ is $h$ in Exercise 25, from which $f^{-1}(g^*(\operatorname{Spec}(C)))=u^*(\operatorname{Spec}(B\otimes_AC))$ is closed.
{{</exercise>}}

{{<exercise 30>}}
Show that the Zariski topology and the constructible topology on $\operatorname{Spec}(A)$ are the same if and only if $A/\mathfrak{N}$ is absolutely flat (where $\mathfrak{N}$ is the nilradical of $A$). [Use Exercise 11.]
QUESTIONANDANSWERSTRING\
We prove that the two topologies coincide if the Zariski topology is Hausdorff, which is because $\operatorname{id}$ is a continuous bijection between a compact space and a Hausdorff space.
{{</exercise>}}

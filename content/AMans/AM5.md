+++
date = '2026-02-18T19:56:49+08:00'
title = "5. Integral Dependence and Valuations"
categories = ["交换代数"]
series = ["Solutions to Atiyah-MacDonald Commutative Algebra"]
+++

You may want to see [this](../am0/) for unclear notations.

---

{{<exercise 1>}}
Let $f:A\to B$ be an integral homomorphism of rings. Show that $f^*:\operatorname{Spec}(B)\to \operatorname{Spec}(A)$ is a *closed* mapping, i.e. that it maps closed sets to closed sets. (This is a geometrical equivalent of (5.10).)
QUESTIONANDANSWERSTRING\
Decompose $f$ as $A\xrightarrow{\pi}\operatorname{im}(f)\xrightarrow{\iota}B$, and hence $f^*=\pi^*\circ\iota^*$. Notice that $\pi$ is a quotient, so $\pi^*$ is the embedding of a closed subspace hence is closed. By definition $\iota$ is integral, by Theorem 5.10 $\iota^*$ is surjective, and therefore it is easy to verify $\iota^*(V(\mathfrak{b}))=V(\mathfrak{b}^c)$ {{<explain>}}See Chapter 1, Exercise 21 iii), every prime ideal on the right is in the left by Theorem 5.11.{{</explain>}}, i.e. $\iota^*$ is closed. Hence $f^*$ is closed.
{{</exercise>}}

{{<exercise 2>}}
Let $A$ be a subring of a ring $B$ such that $B$ is integral over $A$, and let $f:A\to \Omega$ be a homomorphism of $A$ into an algebraically closed field $\Omega$. Show that $f$ can be extended to a homomorphism of $B$ into $\Omega$. [Use (5.10).]
QUESTIONANDANSWERSTRING\
First of all assume that $f$ is injective, and regard $A$ as a subring of $\Omega$. Consider the set \[\Gamma=\{(C,f_C:C\to\Omega):\text{ring }A\subseteq C\subseteq B,f_C|_A=f\}\] with the natural ordering (inclusion of $C$ and restriction of $f_C$), by Zorn's lemma there is a maximal element $(B',f_{B'})$ of $\Gamma$. If $B'\neq B$, obviously we can take $x\in B$ not in $B'$ and consider its minimal polynomial $f$ in $A$, which is also an element of $\Omega[x]$ (this is where we used injectivity), and have a root $x_0$ in $\Omega$. Then we can extend $f_{B'}$ to $B'[x]$ by taking $x_0$ at $x$, which constructs a strictly larger element than $(B', f_{B'})$, contradiction. Hence $B'=B$, and $f$ can indeed be extended.\
Now in the general case, by Theorem 5.10 take prime ideal $\mathfrak{q}$ of $B$ lying over $\ker(f)$ of $A$, then $A/\ker(f)$ can be seen as a subring of $B/\mathfrak{q}$, and the inclusion is integral. By the first part we can construct $B/\mathfrak{q}\to\Omega$, then composing with $B\to B/\mathfrak{q}$ we get the desired extension of $f$.
{{</exercise>}}

{{<exercise 3>}}
Let $f:B\to B'$ be a homomorphism of $A$-algebras, and let $C$ be an $A$-algebra. If $f$ is integral, prove that $f\otimes 1:B\otimes_A C\to B'\otimes_A C$ is integral. (This includes (5.6) ii) as a special case.)
QUESTIONANDANSWERSTRING\
For any $b'\otimes c\in B'\otimes_A C$, if $\sum\limits_{i=0}^nf(b_i){b'}^i=0$, then we have the corresponding \[\sum_{i=0}^n(f\otimes \operatorname{id})(b_i\otimes c^{n-i})~(b'\otimes c)^i=(\sum_{i=0}^nf(b_i){b'}^i)\otimes c^n=0\]
{{</exercise>}}

{{<exercise 4>}}
Let $A$ be a subring of a ring $B$ such that $B$ is integral over $A$. Let $\mathfrak{n}$ be a maximal ideal of $B$ and let $\mathfrak{m}=\mathfrak{n}\cap A$ be the corresponding maximal ideal of $A$. Is $B_\mathfrak{n}$ necessarily integral over $A_\mathfrak{m}$?\
[Consider the subring $k[x^2-1]$ of $k[x]$, where $k$ is a field, and let $\mathfrak{n}=(x-1)$. Can the element $1/(x+1)$ be integral?]
QUESTIONANDANSWERSTRING\
We must let $k$ be a field with characteristic $\neq2$ in the hint; if $1/(x+1)$ is integral on $k[x^2]_{(x^2-1)}$, i.e. \[\frac1{(x+1)^n}=\frac{p_1}{q_1}\frac1{(x+1)^{n-1}}+\cdots+\frac{p_n}{q_n}\] where $q_i\in k[x^2]$ is not divisible by $x^2-1$, then $q_i$ cannot be a multiple of $x+1$, so the two sides of the equality have different powers of $(x+1)$, contradiction.
{{</exercise>}}

{{<exercise 5>}}
Let $A\subseteq B$ be rings, $B$ integral over $A$.
TOMANDJERRYSTRINGLITERAL\
i) If $x\in A$ is a unit in $B$ then it is a unit in $A$.
QUESTIONANDANSWERSTRING\
As $x^{-1}\in B$, we have $x^{-n}+a_1x^{-n+1}+\cdots+a_n=0$, hence $x^{-1}=-a_1-_2x-\cdots-a_nx^{n-1}\in A$.
TOMANDJERRYSTRINGLITERAL\
ii) The Jacobson radical of $A$ is the contraction of the Jacobson radical of $B$.
QUESTIONANDANSWERSTRING\
By Theorem 5.10 and Corollary 5.8 every maximal ideal of $A$ is the contraction of a maximal ideal of $B$. Then the claim is obvious because the Jacobson radical is the intersection of all maximal ideals.
{{</exercise>}}

{{<exercise 6>}}
Let $B_1,\ldots,B_n$ be integral $A$-algebras. Show that $\prod_{i=1}^nB_i$ is an integral $A$-algebra.
QUESTIONANDANSWERSTRING\
For integral $f_i:A\to B_i$ and $(b_i)\in\prod_{i=1}^nB_i$, we have \[(\prod f_i)(A)[(b_i)]\subseteq\prod f_i(A)[b_i]\] whose right hand side is a product of finitely generated $A$ modules hence finitely generated. By Proposition 5.1 $(b_i)$ is integral over $A$.
{{</exercise>}}

{{<exercise 7>}}
Let $A$ be a subring of a ring $B$, such that the set $B-A$ is closed under multiplication. Show that $A$ is integrally closed in $B$.
QUESTIONANDANSWERSTRING\
Suppose $b\in B\backslash A$ is integral over $A$, take minimal $n$ in the equation $b^n+a_1b^{n-1}+\cdots+a_{n-1}b+a_n=0$. By minimality $b^{n-1}+a_1b^{n-2}+\cdots+a_{n-1}\not\in A$, this makes $-a_n\not\in A$, which is contradiction.
{{</exercise>}}

{{<exercise 8>}}
i) Let $A$ be a subring of an integral domain $B$, and let $C$ be the integral closure of $A$ in $B$. Let $f$, $g$ be monic polynomials in $B[x]$ such that $fg\in C[x]$. Then $f$, $g$ are in $C[x]$. [Take a field containing $B$ in which the polynomials $f$, $g$ split into linear factors: say $f=\prod(x-\xi_i)$, $g=\prod(x-\eta_j)$. Each $\xi_i$ and each $\eta_j$ is a root of $fg$, hence is integral over $C$. Hence the coefficients of $f$ and $g$ are integral over $C$.]
QUESTIONANDANSWERSTRING\
The hint is basically the answer; we can take the field to be the algebraic closure of the field of fractions of $B$.
TOMANDJERRYSTRINGLITERAL\
ii) Prove the same result without assuming that $B$ (or $A$) is an integral domain.
QUESTIONANDANSWERSTRING\
Reviewing the proof of i), we only need a ring containing $B$ in which $f$, $g$ both split into linear factors. For this, if suffices to prove that for any non-constant monic polynomial $f\in B[x]$, there is a ring containing $B$ in which $f$ has a root: $B\to B[x]\to B[x]/(f)$ works.
{{</exercise>}}

{{<exercise 9>}}
Let $A$ be a subring of a ring $B$ and let $C$ be the integral closure of $A$ in $B$. Prove that $C[x]$ is the integral closure of $A[x]$ in $B[x]$. [If $f\in B[x]$ is integral over $A[x]$, then \[f^m+g_1f^{m-1}+\cdots+g_m=0\quad(g_i\in A[x]).\] Let $r$ be an integer larger than $m$ and the degrees of $g_1,\ldots,g_m$ and let $f_1=f-x^r$, so that \[(f_1+x^r)^m+g_1(f_1+x^r)^{m-1}+\cdots+g_m=0\] or say \[f_1^m+h_1f_1^{m-1}+\cdots+h_m=0,\] where $h_m=(x^r)^m+g_1(x^r)^{m-1}+\cdots+g_m\in A[x]$. Now apply Exercise 8 to the polynomials $-f_1$ and $f_1^{m-1}+h_1f_1^{m-2}+\cdots+h_{m-1}$.]
QUESTIONANDANSWERSTRING\
The hint is basically the answer, in which $+x^r$ is to make the polynomials monic so that we can apply Exercise 8. The hint already shows that every polynomial integral over $A[x]$ is in $C[x]$, whereas the converse is obvious because integral elements are closed under addition and multiplication.
{{</exercise>}}

{{<exercise 10>}}
A ring homomorphism $f:A\to B$ is said to have the *going-up property* (resp. the *going-down property*) if the conclusion of the going-up theorem (5.11) (resp. the going-down theorem (5.16)) holds for $B$ and its subring $f(A)$.\
Let $f^*:\operatorname{Spec}(B)\to \operatorname{Spec}(A)$ be the mapping associated with $f$.
TOMANDJERRYSTRINGLITERAL\
i) Consider the following three statements:\
(a) $f^*$ is a closed mapping.\
(b) $f$ has the going-up property.\
(c) Let $\mathfrak{q}$ be any prime ideal fo $B$ and let $\mathfrak{p}=\mathfrak{q}^c$. Then $f^*:\operatorname{Spec}(B/\mathfrak{q})\to \operatorname{Spec}(A/\mathfrak{p})$ is surjective.\
Prove that (a) $\Rightarrow$ (b) $\Leftrightarrow$ (c). (See also Chapter 6, Exercise 11.)
QUESTIONANDANSWERSTRING\
a) $\Rightarrow$ c): By Chapter 1, Exercise 21 iii), for $\mathfrak{q}\in\operatorname{Spec}(B)$ we have $f^*(V(\mathfrak{q}))=\overline{f^*(V(\mathfrak{q}))}=V(\mathfrak{q}^c)$, where both sides are identified the sides in c).\
b) $\Leftrightarrow$ c) is a direct rewriting of definition.
TOMANDJERRYSTRINGLITERAL\
ii) Consider the following three statements:\
(a') $f^*$ is an open mapping.\
(b') $f$ has the going-down property.\
(c') For any prime ideal $\mathfrak{q}$ of $B$, if $\mathfrak{p}=\mathfrak{q}^c$, then $f^*:\operatorname{Spec}(B_\mathfrak{q})\to\operatorname{Spec}(A_\mathfrak{p})$ is surjective.\
Prove that (a') $\Rightarrow$ (b') $\Leftrightarrow$ (c'). (See also Chapter 7, Exercise 23.)\
[To prove that (a') $\Rightarrow$ (c'), observe that $B_\mathfrak{q}$ is the direct limit of the rings $B_t$ where $t\in B-\mathfrak{q}$; hence, by Chapter 3, Exercise 26, we have $f^*(\operatorname{Spec}(B_\mathfrak{q}))=\bigcap_{t}f^*(\operatorname{Spec}(B_t))=\bigcap_tf^*(Y_t)$. Since $Y_t$ is an open neighborhood of $\mathfrak{q}$ in $Y$, and since $f^*$ is open, it follows that $f^*(Y_t)$ is an open neighborhood of $\mathfrak{p}$ in $X$ and therefore contains $\operatorname{Spec}(A_\mathfrak{p})$.]
QUESTIONANDANSWERSTRING\
In fact by Chapter 3, Exercise 22, the spectrum of localized rings on a prime ideal is the intersection of all open sets containing it, but under open mappings the images and inverse images of open sets are open, so a') $\Rightarrow$ c') is obvious.\
b') $\Leftrightarrow$ c') is a direct rewriting of definition.
{{</exercise>}}

{{<exercise 11>}}
Let $f:A\to B$ be a flat homomorphism of rings. Then $f$ has the going-down property. [Chapter 3, Exercise 18.] {{<explain>}}The hint is exactly the full answer.{{</explain>}}
{{</exercise>}}

{{<exercise 12>}}
Let $G$ be a finite group of automorphisms of a ring $A$, and let $A^G$ denote the subring of $G$-invariants, that is of all $x\in A$ such that $\sigma(x)=x$ for all $\sigma \in G$. Prove that $A$ is integral over $A^G$. [If $x\in A$, observe that $x$ is a root of the polynomial $\prod_{\sigma\in G}(t-\sigma(x))$.]
QUESTIONANDANSWERSTRING\
The hint is exactly the answer.
TOMANDJERRYSTRINGLITERAL\
Let $S$ be a multiplicatively closed subset of $A$ such that $\sigma(S)\subseteq S$ for all $\sigma\in G$, and let $S^G=S\cap A^G$. Show that the action of $G$ on $A$ extends to an action on $S^{-1}A$, and that $(S^G)^{-1}A^G\simeq (S^{-1}A)^G$.
QUESTIONANDANSWERSTRING\
There is a natural action of $G$ on $S^{-1}A$ given by $\sigma(a/s)=\sigma(a)/\sigma(s)$, which leads to an isomorphism \[f:(S^G)^{-1}A^G\to (S^{-1}A)^G,\quad f(\frac as)=\frac as,\quad f^{-1}(\frac as)=\frac{\sum_{\sigma\in G}\sigma(a)}{\sum_{\sigma\in G}\sigma(s)}\]
{{</exercise>}}

{{<exercise 13>}}
In the situation of Exercise 12, let $\mathfrak{p}$ be a prime ideal of $A^G$, and let $P$ be the set of prime ideals of $A$ whose contraction is $\mathfrak{p}$. Show that $G$ acts transitively on $P$. In particular, $P$ is *finite*.\
[Let $\mathfrak{p}_1,\mathfrak{p}_2\in P$ and let $x\in\mathfrak{p}_1$. Then $\prod_\sigma \sigma(x)\in\mathfrak{p}_1\cap A^G=\mathfrak{p}\subseteq\mathfrak{p}_2$, hence $\sigma(x)\in\mathfrak{p}_2$ for some $\sigma\in G$. Deduce that $\mathfrak{p}_1$ is contained in $\bigcup_{\sigma\in G}\sigma(\mathfrak{p}_2)$, and then apply (1.11) and (5.9).]
QUESTIONANDANSWERSTRING\
It is obvious that $\sigma(P)\subseteq P\forall\sigma\in G$. The hint is basically the answer; from $\sigma(x)\in\mathfrak{p}_2$ for some $\sigma$ we see $x\in\sigma^{-1}(\mathfrak{p}_2)\subseteq\bigcup_{\sigma\in G}\sigma(\mathfrak{p}_2)$, which holds for all $x\in\mathfrak{p}_1$, i.e. $\mathfrak{p}_1\subseteq\bigcup_{\sigma\in G}\sigma(\mathfrak{p}_2)$. By Proposition 1.11 $\mathfrak{p}_1$ is contained in some $\sigma(\mathfrak{p}_2)$, and by Corollary 5.9 $\mathfrak{p}_1=\sigma(\mathfrak{p}_2)$, hence the transitivity.
{{</exercise>}}

{{<exercise 14>}}
Let $A$ be an integrally closed domain, $K$ its field of fractions and $L$ a finite normal separable extension of $K$. Let $G$ b the Galois group of $L$ over $K$ and let $B$ be the integral closure of $A$ in $L$. Show that $\sigma(B)=B$ for all $\sigma\in G$, and that $A=B^G$.
QUESTIONANDANSWERSTRING\
For $x\in B$ consider $x^n+a_1x^{n-1}+\cdots+a_n=0$; under action of $\sigma$ (which is identity on $K$) we see $\sigma(x)$ is integral on $A$, i.e. $\sigma(x)\in B$, $\sigma(B)\subseteq B$. Similarly $\sigma^{-1}(B)\subseteq B$, hence $\sigma(B)=B$.\
Notice that $B^G\subseteq B$ is integral on $A$ and $A\subseteq B^G$, and also $B^G\subseteq L^G=K$, because $A$ is integrally closed in $K$ we have $B^G=A$.
{{</exercise>}}

{{<exercise 15>}}
Let $A$, $K$ be as in Exercise 14, let $L$ b any finite extension field of $K$, and let $B$ be the integral closure of $A$ in $L$. Show that, if $\mathfrak{p}$ is any prime ideal of $A$, then the set of prime ideals $\mathfrak{q}$ of $B$ which contract to $\mathfrak{p}$ is finite (in other words, that $\operatorname{Spec}(B)\to\operatorname{Spec}(A)$ has finite fibers).\
[Reduce to the two cases (a) $L$ separable over $K$ and (b) $L$ purely inseparable over $K$. In case (a), embed $L$ in a finite normal separable extension of $K$, and use Exercises 13 and 14. In case (b), if $\mathfrak{q}$ is a prime ideal of $B$ such that $\mathfrak{q}\cap A=\mathfrak{p}$, show that $\mathfrak{q}$ is the set of all $x\in B$ such that $x^{p^m}\in\mathfrak{p}$ for some $m\ge 0$, where $p$ is the characteristic of $K$, and hence that $\operatorname{Spec}(B)\to\operatorname{Spec}(A)$ is bijective in this case.]
QUESTIONANDANSWERSTRING\
Following the hint, in case (a) embed $L$ into a finite normal separable extension $L'$ of $K$, and assume the integral closure of $A$ in $L'$ is $B'$. Then by Exercise 13 and 14, $\operatorname{Spec}(B')\to\operatorname{Spec}(A)$ has finite fibers. But $B'$ is integral on $B$, so the first part of $\operatorname{Spec}(B')\to\operatorname{Spec}(B)\to\operatorname{Spec}(A)$ is surjective, hence the second part can only have finite fibers.\
In case (b), field theory gives $\operatorname{char}(K)=p>0$ and $\forall x\in L,\exists m,x^{p^m}\in K$, which obviously leads to $\mathfrak{q}=\{x\in B:x^{p^m}\in\mathfrak{p}\text{ for some }m\ge0\}$, finishing the hint (bijection obviously have finite fibers).\
In the general case, field theory says that $L$ is purely inseparable over the maximal separable sub-extension $L'$ of $K$. As the integral closure of integral closure is still the integral closure, stacking the above two cases finishes the proof.
{{</exercise>}}

### *Noether's normalization lemma*

{{<exercise 16>}}
Let $k$ be a field and let $A\neq0$ be a finitely generated $k$-algebra. Then there exist elements $y_1,\ldots,y_r\in A$ which are algebraically independent over $k$ and such that $A$ is integral over $k[y_1,\ldots,y_r]$.\
We shall assume that $k$ is *infinite*. (The result is still true if $k$ is finite, but a different proof is needed.) Let $x_1,\ldots,x_n$ generate $A$ as a $k$-algebra. We can renumber the $x_i$ so that $x_1,\ldots,x_r$ are algebraically independent over $k$ and each of $x_{r+1},\ldots,x_n$ is algebraic over $k[x_1,\ldots,x_n]$ {{<explain>}}Notice here algebraic is not enough; we have to make the polynomials monic.{{</explain>}}. Now proceed by induction on $n$. If $n=r$ there is nothing to do, so suppose $n>r$ and the result true for $n-1$ generators. The generator $x_n$ is algebraic over $k[x_1,\ldots,x_{n-1}]$, hence there exists a polynomial $f\neq0$ in $n$ variables such that $f(x_1,\ldots,x_{n-1},x_n)=0$. Let $F$ be the homogeneous part of highest degree in $f$. Since $k$ is infinite, there exist $\lambda_1,\ldots,\lambda_{n-1}\in k$ such that $F(\lambda_1,\ldots,\lambda_{n-1},1)\neq0$. Put $x_i'=x_i-\lambda_ix_n~(1\le i\le n-1)$. Show that $x_n$ is integral over the ring $A'=k[x_1',\ldots,x_{n-1}']$, and hence that $A$ is integral over $A'$. Then apply the inductive hypothesis to $A'$ to complete the proof.
TOMANDJERRYSTRINGLITERAL\
From the proof it follows that $y_1,\ldots,y_r$ may be taken to be linear combinations of $x_1,\ldots,x_n$. This has the following geometrical interpretation: if $k$ is algebraically closed and $X$ is an affine algebraic variety in $k^n$ with coordinate ring $A\neq0$, then there exists a linear subspace $L$ of dimension $r$ in $k^n$ and a linear mapping of $k^n$ onto $L$ which maps $X$ *onto* $L$. [Use Exercise 2.]
QUESTIONANDANSWERSTRING\
Chapter 1, Exercise 27, 28 show that the coordinate ring functor $A(\cdot):\mathsf{Aff}\to\mathsf{Alg}_k^{\text{op}}$ is an equivalence. We switch to $\mathsf{Alg}_k$: the above result gives \[k[y_1,\ldots,y_r]\xrightarrow{\pi^*}k[x_1,\ldots,x_n]\xrightarrow{\iota^*} A(X)\] so that $\iota^*\circ\pi^*$ is integral and $\pi^*$ is 'linear' (i.e. mapping $y_i$ into a linear combination of $x_i$). Thus under the equivalence $\pi:k^n\to k^r$ is linear.\
To prove that $\pi\circ\iota$ is surjective, we shall only prove that any $\{*\}\to k^r$ can be extended to $\{*\}\to X$; under the equivalence, it suffices to prove that any $k[y_1,\ldots,y_r]\to k$ can be extended to $A(X)\to k$, which is exactly integrality by Exercise 2.
{{</exercise>}}

### *Nullstellensatz* (weak form).

{{<exercise 17>}}
Let $X$ be an affine algebraic variety in $k^n$, where $k$ is an algebraically closed field, and let $I(X)$ be the ideal of $X$ in the polynomial ring $k[t_1,\ldots,t_n]$ (Chapter 1, Exercise 27). If $I(X)\neq(1)$ then $X$ is not empty. [Let $A=k[t_1,\ldots,t_n]/I(X)$ be the coordinate ring of $X$. Then $A\neq0$, hence by Exercise 16 there exists a linear subspace $L$ of dimension $\ge0$ in $k^n$ and a mapping of $X$ *onto* $L$. Hence $X\neq\varnothing$.]
QUESTIONANDANSWERSTRING\
The hint is exactly the answer.
TOMANDJERRYSTRINGLITERAL\
Deduce that every maximal ideal in the ring $k[t_1,\ldots,t_n]$ is of the form $(t_1-a_1,\ldots,t_n-a_n)$ where $a_i\in k$.
QUESTIONANDANSWERSTRING\
Let a maximal ideal be $\mathfrak{m}$, then $k'=k[t_1,\ldots,t_n]/\mathfrak{m}$ is a field, which is a finitely generated $k$-algebra, hence contains some $A=k[s_1,\ldots,s_r]$ on which $k'$ is integral. By Proposition 5.7, $A$ is a field, hence $r=0$, $A=k$. We have $k'$ is integral over $k$, which is algebraically closed, hence $k'=k$, assume under $k[t_1,\ldots,t_n]\to k'=k$ the generators are mapped to $a_i$, then clearly $\mathfrak{m}=(t_1-a_1,\ldots,t_n-a_n)$. {{<explain>}}This proof does not make use of the claim in the first part, which is probably the proof the author wanted in Exercise 19; I cannot find another proof (using the first part) for the time being.{{</explain>}}
{{</exercise>}}

{{<exercise 18>}}
Let $k$ be a field and let $B$ be a finitely generated $k$-algebra. Suppose that $B$ is a field. Then $B$ is a finite algebraic extension of $k$. (This is another version of Hilbert's Nullstellensatz. The following proof is due to Zariski. For other proofs, see (5.24), (7.9).)\
Let $x_1,\ldots,x_n$ generate $B$ as a $k$-algebra. The proof is by induction on $n$. If $n=1$ the result is clearly true, so assume $n>1$. Let $A=k[x_1]$ and let $K=k(x_1)$ be the field of fractions of $A$. By the inductive hypothesis, $B$ is a finite algebraic extension of $K$, hence each of $x_2,\ldots,x_n$ satisfies a monic polynomial equation with coefficients in $K$, i.e. coefficients of the form $a/b$ where $a$ and $b$ are in $A$. If $f$ is the product of the denominators of all these coefficients, then each of $x_2,\ldots,x_n$ is integral over $A_f$. Hence $B$ and therefore $K$ is integral over $A_f$.\
Suppose $x_1$ is transcendental over $k$. Then $A$ is integrally closed, because it is a unique factorization domain. Hence $A_f$ is integrally closed (5.12), and therefore $A_f=K$, which is clearly absurd. Hence $x_1$ is algebraic over $k$, hence $K$ (and therefore $B$) is a finite extension of $k$.
{{</exercise>}}

{{<exercise 19>}}
Deduce the result of Exercise 17 from Exercise 18. {{<explain>}}See explanation at the end of the proof of Exercise 17 part 2.{{</explain>}}
{{</exercise>}}

{{<exercise 20>}}
Let $A$ be a subring of an integral domain $B$ such that $B$ is finitely generated over $A$. Show that there exists $s\neq0$ in $A$ and elements $y_1,\ldots,y_n$ in $B$, algebraically independent over $A$ and such that $B_s$ is integral over $B_s'$, where $B'=A[y_1,\ldots,y_n]$. [Let $S=A-\{0\}$ and let $K=S^{-1}A$, the field of fractions of $A$. Then $S^{-1}B$ is a finitely generated $K$-algebra and therefore by the normalization lemma (Exercise 16) there exist $x_1,\ldots,x_n$ in $S^{-1}B$, algebraically independent over $K$ and such that $S^{-1}B$ is integral over $K[x_1,\ldots,x_n]$. Let $z_1,\ldots,z_n$ generate $B$ as an $A$-algebra. Then each $z_j$ (regarded as an element of $S^{-1}B$) is integral over $K[x_1,\ldots,x_n]$. By writing an equation of integral dependence for each $z_j$, show that there exists $s\in S$ such that $x_i=y_i/s~(1\le i\le n)$ with $y_i\in B$, and such that each $sz_j$ is integral over $B'$. Deduce that this $s$ satisfies the conditions stated.]
QUESTIONANDANSWERSTRING\
The $s$ in the hint can be taken to be the product of all denominators of $x_i$ and all (non-leading) coefficients of the integral dependence equations of $z_j$. Thus $z_j$ is integral over $B_s'$, hence $B_s=B_s'[z_1,\ldots,z_n]$ is integral over $B_s'$. $y_i$ are algebraically independent over $A$ because $x_i$ are so.
{{</exercise>}}

{{<exercise 21>}}
Let $A$, $B$ be as in Exercise 20. Show that there exists $s\neq0$ in $A$ such that, if $\Omega$ is an algebraically closed field and $f:A\to \Omega$ is a homomorphism for which $f(s)\neq0$, then $f$ can be extended to a homomorphism $B\to \Omega$. [With the notation of Exercise 20, $f$ can be extended first of all to $B'$, for example by mapping each $y_i$ to 0; then to $B_s'$ (because $f(s)\neq0$), and finally to $B_s$ (by Exercise 2, because $B_s$ is integral over $B_s'$).] {{<explain>}}The hint is exactly the answer, just taking restriction to $B$ afterwards.{{</explain>}}
{{</exercise>}}

{{<exercise 22>}}
Let $A$, $B$ be as in Exercise 20. If the Jacobson radical of $A$ is zero, then so is the Jacobson radical of $B$.\
[Let $v\neq0$ be an element of $B$. We have to show that there is a maximal ideal of $B$ which does not contain $v$. By applying Exercise 21 to the ring $B_v$, and its subring $A$, we obtain an element $s\neq0$ in $A$. Let $\mathfrak{m}$ be a maximal ideal of $A$ such that $s\not\in\mathfrak{m}$, and let $k=A/\mathfrak{m}$. Then the canonical mapping $A\to k$ extends to a homomorphism $g$ of $B_v$ into an algebraic closure $\Omega$ of $k$. Show that $g(v)\neq0$ and that $\ker(g)\cap B$ is a maximal ideal of $B$.]
QUESTIONANDANSWERSTRING\
We follow the hint. $g(v)$ is obviously non-zero because $v$ is invertible in $B_v$. Notice that $\ker(g)\cap A=\mathfrak{m}$ is maximal, hence $\mathfrak{m}_s\subsetneq A_s$ is maximal {{<explain>}}by the prime ideal correspondence, as $s\not\in\mathfrak{m}${{</explain>}}. Recall that in the proof of Exercise 21, we can choose $y_i$ to be mapped to $0$, hence in $B_s'$ the kernel of $g$ is $\mathfrak{m}_s[y_1,\ldots,y_n]$, which is a maximal ideal of $B_s'$. By Corollary 5.8 $\ker(g)$ is maximal in $(B_v)_s$, and by the prime ideal correspondence $\ker(g)$ is maximal in $B_v$.\
We then prove that $\ker(g)\cap B$ is coprime with $(v)$ in $B$; this is because $g(v)\in\Omega$ satisfy some polynomial equation with coefficients in $k\subseteq g(B)$, e.g. $1+g(b_1)g(v)+\cdots+g(b_m)g(v)^m=0$ {{<explain>}}here we can make the constant term $1$ because $k$ is a field{{</explain>}}, hence $1+b_1v+\cdots+b_mv^m\in\ker(g)\cap B$, i.e. $\ker(g)\cap B+(v)=B$.\
This proves that there is no maximal ideal containing $v$ and $\ker(g)\cap B$ in $B$, by prime ideal correspondence from $B_v$ we get $\ker(g)\cap B$ is maximal in $B$.
{{</exercise>}}

{{<exercise 23>}}
Let $A$ be a ring. Show that the following are equivalent:\
i) Every prime ideal in $A$ is an intersection of maximal ideals.\
ii) In very homomorphism image of $A$ the nilradical is equal to the Jacobson radical.\
iii) Every prime ideal in $A$ which is not maximal is equal to the intersection of the prime ideals which contain it strictly.\
[The only hard part is iii) $\Rightarrow$ ii). Suppose ii) false, then there is a prime ideal which is not an intersection of maximal ideals. Passing to the quotient ring, we may assume that $A$ is an integral domain whose Jacobson radical $\mathfrak{R}$ is not zero. Let $f$ be a non-zero element of $\mathfrak{R}$. Then $A_f\neq0$, hence $A_f$ has a maximal ideal, whose contraction in $A$ is a prime ideal $\mathfrak{p}$ such that $f\not\in\mathfrak{p}$, and which is maximal with respect to this property. Then $\mathfrak{p}$ is not maximal and is not equal to the intersection of the prime ideals strictly containing $\mathfrak{p}$.] {{<explain>}}The hint is exactly the answer.{{</explain>}}\
A ring $A$ with the three equivalent properties above is called a *Jacobson ring*.
{{</exercise>}}

{{<exercise 24>}}
Let $A$ be a Jacobson ring (Exercise 23) and $B$ an $A$-algebra. Show that if $B$ is either (i) integral over $A$ or (ii) finitely generated as an $A$-algebra, then $B$ is Jacobson. [Use Exercise 22 for (ii).]
QUESTIONANDANSWERSTRING\
For ii): For any $\mathfrak{q}\in\operatorname{Spec}(B)$, $B/\mathfrak{q}$ is finitely generated on $A/\mathfrak{q}^c$, whose Jacobson radical is equal to its nilradical, which is $0$, hence by Exercise 22 $B/\mathfrak{q}$ also has zero Jacobson radical, which expresses $\mathfrak{q}$ as an intersection of maximal ideals under the ideal correspondence.\
For i): by replacing $A$ with its image, we can assume $A\subseteq B$. We only need to prove for any $\mathfrak{q}\in\operatorname{Spec}(B)$, it is the intersection of all maximal ideals containing it; take $b$ in the aforementioned intersection, then $A[b]$ is also Jacobson by ii), hence we can assume $b\in A$, by Exercise 5 ii) \[0=\mathfrak{R}_{A/\mathfrak{q}^c}=\mathfrak{R}_{B/\mathfrak{q}}\cap A/\mathfrak{q}^c\ni\overline{b}\] i.e. $b\in\mathfrak{q}$.
TOMANDJERRYSTRINGLITERAL\
In particular, every finitely generated ring, and every finitely generated algebra over a field, is a Jacobson ring. {{<explain>}}which results from the fact that every field and the integer ring is Jacobson.{{</explain>}}
{{</exercise>}}

{{<exercise 25>}}
Let $A$ be a ring. Show that the following are equivalent:\
i) $A$ is a Jacobson ring;\
ii) Every finitely generated $A$-algebra $B$ which is a field is finite over $A$.\
[i) $\Rightarrow$ i). Reduce to the case where $A$ is a subring of $B$, and use Exercise 21. If $s\in A$ is as in Exercise 21, then there exists a maximal ideal $\mathfrak{m}$ of $A$ not containing $s$, and the homomorphism $A\to A/\mathfrak{m}=k$ extends to a homomorphism $g$ of $B$ into the algebraic closure of $k$. Since $B$ is a field, $g$ in injective, and $g(B)$ is algebraic over $k$, hence finite algebraic over $k$.\
ii) $\Rightarrow$ i). Use criterion iii) of Exercise 23. Let $\mathfrak{p}$ be a prime ideal of $A$ which is not maximal, and let $B=A/\mathfrak{p}$. Let $f$ be a non-zero element of $B$. Then $B_f$ is a finitely generated $A$-algebra. If it is a field it is finite over $B$, hence integral over $B$ and therefore $B$ is a field by (5.7). Hence $B_f$ is not a field and therefore has a non-zero prime ideal, whose contraction in $B$ is a non-zero ideal $\mathfrak{p}'$ such that $f\not\in\mathfrak{p}'$.] {{<explain>}}The hint is exactly the answer.{{</explain>}}
{{</exercise>}}

{{<exercise 26>}}
Let $X$ be a topological space. A subset of $X$ is *locally closed* if it is the intersection of an open set and a closed set, or equivalently if it is open in its closure.\
The following conditions on a subset $X_0$ of $X$ are equivalent:\
(1) Every non-empty locally closed subset of $X$ meets $X_0$;\
(2) For every closed set $E$ in $X$ we have $\overline{E\cap X_0}=E$;\
(3) The mapping $U\mapsto U\cap X_0$ of the collection of open sets of $X$ onto the collection of open sets of $X_0$ is *bijective*.
QUESTIONANDANSWERSTRING\
(1) $\Rightarrow$ (2): $\subseteq$ is obvious. Every open set of $E$ is locally closed, hence intersects $X_0$, hence $\supseteq$.\
(2) $\Rightarrow$ (3): the inverse is given by $U'\mapsto X\backslash\overline{(X_0\backslash U')}$.\
(3) $\Rightarrow$ (1): if a locally closed set $U\cap C$ does not intersects $X_0$, then $U\cap X_0=(U\cap(X\backslash C))\cap X_0$, which means $U=U\cap(X\backslash C)$, i.e. $U\cap C=\varnothing$.
TOMANDJERRYSTRINGLITERAL\
A subset $X_0$ satisfying these conditions is said to be *very dense* in $X$.
TOMANDJERRYSTRINGLITERAL\
If $A$ is a ring, show that the following are equivalent:\
i) $A$ is a Jacobson ring;\
ii) The set of maximal ideals of $A$ is very dense in $\operatorname{Spec}(A)$;\
iii) Every locally closed subset of $\operatorname{Spec}(A)$ consisting of a single point is closed.\
[ii) and iii) are geometrical formulations of conditions ii) and iii) of Exercise 23.]
QUESTIONANDANSWERSTRING\
It is obvious that i) $\Leftrightarrow$ ii) $\Rightarrow$ iii). For iii) $\Rightarrow$ i): the locally closed singletons of $\operatorname{Spec}(A)$ can be written as $\{\mathfrak{p}\}=V(\mathfrak{a})\backslash V(\mathfrak{b})$, which means every prime ideal strictly containing $\mathfrak{p}$ contains $r(\mathfrak{p}+\mathfrak{b})$, i.e. $\mathfrak{p}$ is not the intersection of the maximal ideal containing it; by condition every such $\mathfrak{p}$ must have $\{\mathfrak{p}\}$ is closed, i.e. $\mathfrak{p}$ is maximal, hence $A$ is Jacobson.
{{</exercise>}}

### *Valuation rings and valuations*

{{<exercise 27>}}
Let $A$, $B$ be two local rings. $B$ is said to *dominate* $A$ if $A$ is a subring of $B$ and the maximal ideal $\mathfrak{m}$ of $A$ is contained in the maximal ideal $\mathfrak{n}$ of $B$ (or, equivalently, if $\mathfrak{m}=\mathfrak{n}\cap A$). Let $K$ be a field and let $\Sigma$ be the set of all local subrings of $K$. If $\Sigma$ is ordered by the relation of domination, show that $\Sigma$ has maximal elements and that $A\in\Sigma$ is maximal if and only if $A$ is a valuation ring of $K$. [Use (5.21).]
QUESTIONANDANSWERSTRING\
Let $A$ be a valuation ring of $K$ with maximal ideal $\mathfrak{m}$, and local ring $B$ dominates $A$, with maximal ideal $\mathfrak{n}$. By Proposition 5.18 ii), $B$ is also a valuation ring. Notice that $\mathfrak{m}\backslash\{0\}=(K\backslash A)^{-1}$ and the same for $B$, hence $B\subseteq A$. This proves that valuation rings are maximal in $\Sigma$.\
Conversely, let $A$ be a maximal element of $\Sigma$ with maximal ideal $\mathfrak{m}$. Consider $f:A\to A/\mathfrak{m}\to\overline{A/\mathfrak{m}}$ (algebraic closure); $(A,f)$ is an element of the '$\Sigma$' defined after Proposition 5.18. It is proven that its maximal elements are local with maximal ideal $\ker(f)$, and maximality here implies maximality there, hence $A$ can only be a valuation ring.
{{</exercise>}}

{{<exercise 28>}}
Let $A$ be an integral domain, $K$ its field of fractions. Show that the following are equivalent:\
(1) $A$ is a valuation ring of $K$;\
(2) If $\mathfrak{a}$, $\mathfrak{b}$ are any two ideals of $A$, then either $\mathfrak{a}\subseteq\mathfrak{b}$ or $\mathfrak{b}\subseteq\mathfrak{a}$.
QUESTIONANDANSWERSTRING\
i) $\Rightarrow$ ii): for ideals $\mathfrak{a},\mathfrak{b}$, if we ca pick $a\in\mathfrak{a}\backslash\mathfrak{b}$ and $0\neq b\in\mathfrak{b}$, because $a/b\not\in A$, we must have $b/a\in A$, hence $b\in\mathfrak{a}$. The rest is obvious.\
ii) $\Rightarrow$ i): for any $a/b\in K$, the order of $(a)$ and $(b)$ translates to $a/b\in A$ or $b/a\in A$.
TOMANDJERRYSTRINGLITERAL\
Deduce that if $A$ is a valuation ring and $\mathfrak{p}$ is a prime ideal of $A$, then $A_\mathfrak{p}$ and $A/\mathfrak{p}$ are valuation rings of their fields of fractions.
QUESTIONANDANSWERSTRING\
They preserve the total ordering on ideals.
{{</exercise>}}

{{<exercise 29>}}
Let $A$ be a valuation ring of a field $K$. Show that every subring of $K$ which contains $A$ is a local ring of $A$ {{<explain>}}i.e., some localization of $A${{</explain>}}.
QUESTIONANDANSWERSTRING\
Let $A\subseteq B\subseteq K$, hence $B$ is also a valuation ring. Let the maximal ideal of $B$ be $\mathfrak{n}$ and the maximal ideal of $A$ be $\mathfrak{m}$, then \[\mathfrak{n}=(K\backslash B)^{-1}\cup\{0\}\subseteq(K\backslash A)^{-1}\cup\{0\}=\mathfrak{m}\subseteq A\] by definition it is easy to verify $\mathfrak{n}$ is actually a prime ideal of $A$, hence $B=K\backslash(\mathfrak{n}\backslash\{0\})^{-1}=A_\mathfrak{n}$.
{{</exercise>}}

{{<exercise 30>}}
Let $A$ be a valuation ring of a field $K$. The group $U$ of units of $A$ is a subgroup of the multiplicative group $K^*$ of $K$.\
Let $\Gamma=K^*/U$. If $\xi, \eta\in \Gamma$ are represented by $x,y\in K$, define $\xi\ge\eta$ to mean $xy^{-1}\in A$. Show that this defines a total ordering on $\Gamma$ which is compatible with the group structure (i.e., $\xi\ge\eta\Rightarrow\xi\omega\ge\eta\omega$ for all $\omega\in\Gamma$). In other words, $\Gamma$ is a totally ordered abelian group. It is called the *value group* of $A$.
QUESTIONANDANSWERSTRING\
They are trivial verifications.
TOMANDJERRYSTRINGLITERAL\
Let $v:K^*\to\Gamma$ be the canonical homomorphism. Show that $v(x+y)\ge\min(v(x),v(y))$ for all $x,y\in K^*$.
QUESTIONANDANSWERSTRING\
At least one of $K\ni 1+x/y=(x+y)/x$ and $K\ni 1+y/x=(x+y)/y$ must hold.
{{</exercise>}}

{{<exercise 31>}}
Conversely, let $\Gamma$ be a totally ordered abelian group (written *additively*), and let $K$ be a field. A *valuation of $K$ with values in $\Gamma$* is a mapping $v:K^*\to\Gamma$ such that\
(1) $v(xy)=v(x)+v(y)$,\
(2) $v(x+y)\ge\min(v(x),v(y))$,\
for all $x,y\in K$. Show that the set of elements $x\in K^*$ such that $v(x)\ge0$ is a valuation ring of $K$. This ring is called the *valuation ring* of $v$, and the subgroup $v(K^*)$ of $\Gamma$ is the *value group* of $v$.
QUESTIONANDANSWERSTRING\
$v^{-1}(\Gamma_{\ge0})$ is obviously a ring, with maximal ideal $v^{-1}(\Gamma_{>0})$. The rest is trivial.
TOMANDJERRYSTRINGLITERAL\
Thus the concepts of valuation ring and valuation are essentially equivalent.
{{</exercise>}}

{{<exercise 32>}}
Let $\Gamma$ be a totally ordered abelian group. A subgroup $\Delta$ of $\Gamma$ is *isolated* in $\Gamma$ if, whenever $0\le\beta\le\alpha$ and $\alpha\in\Delta$, we have $\beta\in\Delta$. Let $A$ be a valuation ring of a field $K$, with value group $\Gamma$ (Exercise 31). If $\mathfrak{p}$ is a prime ideal of $A$, show that $v(A-\mathfrak{p})$ is the set of elements $\ge0$ in an isolated subgroup $\Delta$ of $\Gamma$, and that the mapping so defined of $\operatorname{Spec}(A)$ into the set of isolated subgroups of $\Gamma$ is bijective.
QUESTIONANDANSWERSTRING\
We define $\Delta=v(A\backslash\mathfrak{p})\cup -v(A\backslash\mathfrak{p})$, which is easy to verify that it is a subgroup of $\Gamma$. We then prove it is isolated: let $0\le\beta\le\alpha=v(x)$ with $x\in A\backslash\mathfrak{p}$, then $\beta\ge0$ means $\beta=v(y)$ for some $y\in A$, and $v(x/y)=\alpha-\beta\ge0$ means $x/y\in A$. Hence we must have $y\not\in\mathfrak{p}$, i.e. $\beta\in\Delta$.\
It is easy to verify that for any isolated subgroup $\Delta$, the ideal $\mathfrak{p}=A\backslash v^{-1}(\Delta)$ is a prime ideal of $A$, and this is inverse to the mapping before.
TOMANDJERRYSTRINGLITERAL\
If $\mathfrak{p}$ is a prime ideal of $A$, what are the value groups of the valuation rings $A/\mathfrak{p}$, $A_\mathfrak{p}$? 
QUESTIONANDANSWERSTRING\
For $A/\mathfrak{p}$, we first prove that if $x,y\in A\backslash\mathfrak{p}$ have the same image in $A/\mathfrak{p}$, then $v(x)=v(y)$; this is because we can assume $xy^{-1}\in A$, and $\mathfrak{p}\ni x-y=y(xy^{-1}-1)$ which forces $xy^{-1}-1\in\mathfrak{p}$. If $v(xy^{-1})>0$ then $xy^{-1}$ is in the maximal ideal of $A$, which must contain $\mathfrak{p}$, which means $1$ is also in the maximal ideal, contradiction. Then $v(xy^{-1})=0$, i.e. $v(x)=v(y)$. We can then define valuation \[\overline{v}:A/\mathfrak{p}\to\Gamma(\cup\{\infty\}),\quad\overline{v}(\overline{x})=\begin{cases}v(x)&x\not\in\mathfrak{p}\\\infty&x\in\mathfrak{p}\end{cases}\] and extend it to the field of fractions of $A/\mathfrak{p}$, whose valuation ring is $A/\mathfrak{p}$ and value group is $\Delta$.\
For $A_\mathfrak{p}$, directly from definition in Exercise 30, $K^*$ stays the same but the unit group $U'$ is now $(A\backslash\mathfrak{p})_\mathfrak{p}$, which is mapped to exactly $\Delta$ under $v$. Hence \[K^*/U'=(K^*/U)/(U'/U)=\Gamma/v(U')=\Gamma/Delta\] which is the value group of $A_\mathfrak{p}$. {{<explain>}}One can also guess the answer by observing that the operations gives an order-reversing correspondence between $\operatorname{Spec}(A)$ and all isolated subgroups.{{</explain>}}
{{</exercise>}}

{{<exercise 33>}}
Let $\Gamma$ be a totally ordered abelian group. We shall show how to construct a field $K$ and a valuation $v$ of $K$ with $\Gamma$ as value group. Let $k$ be any field and let $A=k[\Gamma]$ be the group algebra of $\Gamma$ over $k$. By definition, $A$ is freely generated as a $k$-vector space by elements $x_\alpha(\alpha\in\Gamma)$ such that $x_\alpha x_\beta=x_{\alpha\beta}$. Show that $A$ is an integral domain.\
If $u=\lambda_1x_{\alpha_1}+\cdots+\lambda_nx_{\alpha_n}$ is any non-zero element of $A$, where the $\lambda_i$ are all $\neq0$ and $\alpha_1<\cdots<\alpha_n$, define $v_0(u)$ to be $\alpha_1$. Show that the mapping $v_0:A-\{0\}\to\Gamma$ satisfies the conditions (1) and (2) of Exercise 31.
QUESTIONANDANSWERSTRING\
The equality $v_0(xy)=v_0(x)+v_0(y)$ can also be used to show that $A$ is an integral domain. $v_0(x+y)\ge\mi(v(x),v(y))$ is also nearly trivial.
TOMANDJERRYSTRINGLITERAL\
Let $K$ be the field of fractions of $A$. Show that $v_0$ can be uniquely extended to a valuation $v$ of $K$, and that the value group of $v$ is precisely $\Gamma$.
{{</exercise>}}

{{<exercise 34>}}
Let $A$ b a valuation ring and $K$ its field of fractions. Let $f:A\to B$ be a ring homomorphism such that $f^*:\operatorname{Spec}(B)\to\operatorname{Spec}(A)$ is a *closed* mapping. Then if $g:B\to K$ is any $A$-algebra homomorphism (i.e., if $g\circ f$ is the embedding of $A$ in $K$) we have $g(B)=A$.\
[Let $C=g(B)$; obviously $C\supseteq A$. Let $\mathfrak{n}$ be a maximal ideal of $C$. Since $f^*$ is closed, $\mathfrak{m}=\mathfrak{n}\cap A$ is the maximal ideal of $A$, whence $A_\mathfrak{m}=A$. Also the local ring $C_\mathfrak{n}$ dominates $A_\mathfrak{m}$. Hence by Exercise 27 we have $C_\mathfrak{n}=A$ and therefore $C\subseteq A$.] {{<explain>}}The hint is exactly the answer.{{</explain>}}
{{</exercise>}}

{{<exercise 35>}}
From Exercises 1 and 3 it follows that, if $f:A\to B$ is integral and $C$ is any $A$-algebra, then the mapping $(f\otimes 1)^*:\operatorname{Spec}(B\otimes_A C)\to\operatorname{Spec}(C)$ is a closed map.\
Conversely, suppose that $f:A\to B$ has this property ad that $B$ is an integral domain. Then $f$ is integral. [Replacing $A$ by its image in $B$, reduce to the case where $A\subseteq B$ and $f$ is the injection. Let $K$ be the field of fractions of $B$ and let $A'$ be a valuation ring of $K$ containing $A$. By (5.22) it is enough to show that $A'$ contains $B$. By hypothesis $\operatorname{Spec}(B\otimes_AA')\to\operatorname{Spec}(A')$ is a closed map. Apply the result of Exercise 34 to the homomorphism $B\otimes_AA'\to K$ defined by $b\otimes a'\mapsto ba'$. It follows that $ba'\in A'$ for all $b\in B$ and all $a'\in A'$; taking $a'=1$, we have what we want.]\
Show that the result just proved remains valid if $B$ is a ring with only finitely many minimal prime ideals (e.g., if $B$ is Noetherian). [Let $\mathfrak{p}_i$ be the minimal prime ideals. Then each composite homomorphism $A\to B\to B/\mathfrak{p}_i$ is integral, hence $A\to\prod(B/\mathfrak{p}_i)$ is integral, hence $A\to B/\mathfrak{N}$ is integral (where $\mathfrak{N}$ is the nilradical of $B$), hence finally $A\to B$ is integral.] {{<explain>}}The hints are exactly the answers.{{</explain>}}
{{</exercise>}}

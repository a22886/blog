+++
date = '2026-01-29T16:48:48+08:00'
title = "2. Modules"
categories = ["交换代数"]
series = ["Solutions to Atiyah-MacDonald Commutative Algebra"]
+++

You may want to see [this](../am0/) for unclear notations.

---

{{<exercise 1>}}
Show that $(\mathbf{Z}/m\mathbf{Z}) \otimes_{\mathbf{Z}} (\mathbf{Z}/n\mathbf{Z}) = 0$ if $m$, $n$ are coprime.
QUESTIONANDANSWERSTRING\
By Bez&oacute;ut's theorem there are $p,q\in\mathbf{Z}$ such that $pm+qn=1$, hence \[1\otimes1=1\otimes(1-qn)=1\otimes pm=m\otimes p=0\] and generally $a\otimes b=ab(1\otimes 1)=0$.
{{</exercise>}}

{{<exercise 2>}}
Let $A$ be a ring, $\mathfrak{a}$ an ideal, $M$ and $A$-module. Show that $(A/\mathfrak{a})\otimes_{A}M$ is isomorphic to $M/\mathfrak{a}M$.\
[Tensor the exact sequence $0\to\mathfrak{a}\to A\to A/\mathfrak{a}\to 0$ with $M$.]
QUESTIONANDANSWERSTRING\
Every element of $(A/\mathfrak{a})\otimes_A M$ is of the form \[\sum\overline{a_i}\otimes m_i=\sum a_i(\overline{1}\otimes m_i)=\overline{1}\otimes(\sum a_im_i)\] hence we have bijection \[(A/\mathfrak{a})\otimes_AM\xleftrightarrow{\overline{1}\otimes m\leftrightarrow\overline{m}}M/\mathfrak{a}M\]
The interested reader may also follow the hint, or even verify by the universal property.
{{</exercise>}}

{{<exercise 3>}}
Let $A$ be a local ring, $M$ and $N$ finitely generated $A$-modules. Prove that if $M\otimes N=0$, then $M=0$ or $N=0$.\
[Let $\mathfrak{m}$ be the maximal ideal, $k=A/\mathfrak{m}$ the residue field. Let $M_k=k\otimes_A M\simeq M/\mathfrak{m}M$ by Exercise 2. By Nakayama's lemma, $M_k=0\Rightarrow M=0$. But $M\otimes_A N=0\Rightarrow(M\otimes_A N)_k=0\Rightarrow M_k\otimes_k N_k=0\Rightarrow M_k=0\text{ or }N_k=0$, since $M_k$, $N_k$ are vector spaces over a field.]
QUESTIONANDANSWERSTRING\
One must convince himself that $(M\otimes_A N)_k=M_k\otimes_A N_k=M_k\otimes_k N_k$. The rest is just the hint.
{{</exercise>}}

{{<exercise 4>}}
Let $M_i(i\in I)$ be any family of $A$-modules, and let $M$ be their direct sum. Prove that $M$ is flat $\Leftrightarrow$ each $M_i$ is flat.
QUESTIONANDANSWERSTRING\
In view of the natural isomorphism \[(\bigoplus M_i)\otimes_A \bullet\simeq\bigoplus(M_i\otimes_A \bullet)\] for any injection $f:N'\to N$, $\operatorname{id}_{\bigoplus M_i}\otimes f$ corresponds to $\bigoplus(\operatorname{id}_{M_i}\otimes f)$, but $\bigoplus f_i$ injective is equivalent to $f_i$ all injective, hence the result {{<explain>}}Proposition 2.19{{</explain>}}.
{{</exercise>}}

{{<exercise 5>}}
Let $A[x]$ be the ring of polynomials in one indeterminate over a ring $A$. Prove that $A[x]$ is a flat $A$-algebra. [Use Exercise 4.]
QUESTIONANDANSWERSTRING\
$A[x]=\bigoplus_{n\ge 0}Ax^n$ with each summand isomorphic to $A$ as an $A$-module, obviously flat, hence by Exercise 4 $A[x]$ is flat.
{{</exercise>}}

{{<exercise 6>}}
For any $A$-module, let $M[x]$ denote the set of all polynomials in $x$ with coefficients in $M$, that is to say expressions of the form \[m_0+m_1x+\cdots+m_rx^r\quad(m_i\in M)\] Defining the product of an element of $A[x]$ and an element of $M[x]$ in the obvious way, show that $M[x]$ is an $A[x]$-module.\
Show that $M[x]\simeq A[x]\otimes_A M$.
QUESTIONANDANSWERSTRING\
Both are trivial verifications.
{{</exercise>}}

{{<exercise 7>}}
Let $\mathfrak{p}$ be a prime ideal in $A$. Show that $\mathfrak{p}[x]$ is a prime ideal in $A[x]$. 
QUESTIONANDANSWERSTRING\
$A[x]/\mathfrak{p}[x]\simeq(A/\mathfrak{p})[x]$ is integral by Chapter 1, Exercise 2 iii).
TOMANDJERRYSTRINGLITERAL\
If $\mathfrak{m}$ is a maximal ideal in $A$, is $\mathfrak{m}[x]$ a maximal ideal in $A[x]$?
QUESTIONANDANSWERSTRING\
No, because $\mathfrak{m}[x]\subsetneq\mathfrak{m}+(x)\subsetneq A[x]$.
{{</exercise>}}

{{<exercise 8>}}
i) If $M$ and $N$ are flat $A$-modules, then so is $M\otimes_A N$.
QUESTIONANDANSWERSTRING\
Successive tensor preserves injections {{<explain>}}Proposition 2.19{{</explain>}}.
TOMANDJERRYSTRINGLITERAL\
ii) If $B$ is a flat $A$-algebra and $N$ is a flat $B$-module, then $N$ is flat as an $A$-module.
QUESTIONANDANSWERSTRING\
$N\otimes_A\bullet\simeq N\otimes_B(B\otimes_A\bullet)$ preserves injections {{<explain>}}Proposition 2.19{{</explain>}}.
{{</exercise>}}

{{<exercise 9>}}
Let $0\to M'\to M\to M''\to0$ be an exact sequence of $A$-modules. If $M'$ and $M''$ are finitely generated, then so is $M$.
QUESTIONANDANSWERSTRING\
Let $m_i'$ generate $M'$ and $m_j''$ generate $M''$. Label the homomorphisms by $f:M'\to M$ and $g:M\to M''$. Take any $m_j\in g^{-1}(m_j'')$.\
For any $m\in M$ let $g(m)=\sum a_j''m_j''$, by exactness $m-\sum a_j''m_j\in\operatorname{im}(f)$, i.e., $m-\sum a_j''m_j=f(\sum a_i'm_i')$. Hence $m=\sum a_j''m_j+\sum a_i'f(m_i')$, so the $m_j$ and $f(m_i')$ generate $M$.
{{</exercise>}}

{{<exercise 10>}}
Let $A$ be a ring, $\mathfrak{a}$ an ideal contained in the Jacobson radical of $A$; let $M$ be an $A$-module, and let $u:M\to N$ be a homomorphism. If the induced homomorphism $M/\mathfrak{a}M\to N/\mathfrak{a}N$ is surjective, then $u$ is surjective.
QUESTIONANDANSWERSTRING\
Tensors preserve cokernels, hence \[0=\operatorname{coker}[M/\mathfrak{a}M\to N/\mathfrak{a}N]=\operatorname{coker}(u)\otimes_A(A/\mathfrak{a})=\operatorname{coker}(u)/\mathfrak{a}\operatorname{coker}(u)\] by Exercise 2. But $\operatorname{coker}(u)$ is the quotient of a finitely generated module, hence finitely generated, hence by Nakayama's lemma $\operatorname{coker}(u)=0$, i.e., $u$ is surjective.
{{</exercise>}}

{{<exercise 11>}}
Let $A$ be a ring $\neq0$. Show that $A^m\simeq A^n\Rightarrow m=n$.\
[Let $\mathfrak{m}$ be a maximal ideal of $A$ and let $\phi:A^m\to A^n$ be an isomorphism. Then $1\otimes\phi:(A/\mathfrak{m})\otimes A^m\to(A/\mathfrak{m})\otimes A^n$ is an isomorphism between vector spaces of dimensions $m$ and $n$ over the field $k=A/\mathfrak{m}$. Hence $m=n$.] (Cf. Chapter 3, Exercise 15.) {{<explain>}}The hint is exactly the answer.{{</explain>}}
TOMANDJERRYSTRINGLITERAL\
If $\phi:A^m\to A^n$ is surjective, then $m\ge n$.
QUESTIONANDANSWERSTRING\
The proof is similar to above, notice that tensor products preserve surjections and low dimensional vector spaces cannot surject into high dimensional ones.
TOMANDJERRYSTRINGLITERAL\
If $\phi:A^m\to A^n$ is injective, is it always the case that $m\le n$?
QUESTIONANDANSWERSTRING\
Yes. We will prove that if $m>n$, then any $\phi:A^m\to A^n$ is not injective.\
Let $\iota:A^n\to A^m$ be the embedding to the first $n$ coordinates. By Proposition 2.4, there is an equation \[(\iota\phi)^p+a_1(\iota\phi)^{p-1}+\cdots+a_p(\operatorname{id}_{A^m})=0\] Take such $p$ minimal. Acting on $(0,\ldots,0,1)$ shows that $a_p=0$, hence \[(\iota\phi)\underbrace{((\iota\phi)^{p-1}+\cdots+a_{p-1}(\operatorname{id}_{A^m}))}_{\phi'}=0\] by minimality of $p$ we have $\phi'\neq0$, so that $\ker(\phi)=\ker(\iota\phi)\supseteq\operatorname{im}(\phi')\neq0$, i.e. $\phi$ is not injective.
{{</exercise>}}

{{<exercise 12>}}
Let $M$ be a finitely generated $A$-module and $\phi:M\to A^n$ a surjective homomorphism. Show that $\ker(\phi)$ is finitely generated.\
[Let $e_1,\ldots,e_n$ be a basis of $A^n$ and choose $u_i\in M$ such that $\phi(u_i)=e_i(1\le i\le n)$. Show that $M$ is the direct sum of $\ker(\phi)$ and the submodule generated by $u_1,\ldots,u_n$.]
QUESTIONANDANSWERSTRING\
One can verify the hint quite straightforwardly, from which we know $\ker(\phi)$ is the quotient of a finitely generated module hence finitely generated.
{{</exercise>}}

{{<exercise 13>}}
Let $f:A\to B$ be a ring homomorphism, and let $N$ be a $B$-module. Regarding $N$ as an $A$-module by restriction of scalars, form the $B$-module $N_B=B\otimes_A N$. Show that the homomorphism $g:N\to N_B$ which maps $y$ to $1\otimes y$ is injective and that $g(N)$ is a direct summand of $N_B$.\
[Define $p:N_B\to N$ by $p(b\otimes y)=by$, and show that $N_B=\operatorname{im}(g)\oplus\ker(p)$.]
QUESTIONANDANSWERSTRING\
Following the hint we see $pg=\operatorname{id}_N$, hence $g$ is injective; the exact sequence \[0\to\ker(p)\to N_B\xrightarrow{p}N\to0\] splits, hence $g$ embeds $N$ as a direct summand of $N_B$ {{<explain>}}See 李文威《代数学方法（卷一）》for more.{{</explain>}}.
{{</exercise>}}

### *Direct Limits* {{<explain>}}See 李文威《代数学方法（卷一）》for more details (which here means I am too lazy to write them).{{</explain>}}

{{<exercise 14>}}
A partially ordered set $I$ is said to be a directed set if for each pair $i$, $j$ in $I$ there exists $k\in I$ such that $i\le k$ and $j\le k$.\
Let A be a ring, let $I$ be a directed set and let $(M_i)_{i\in I}$ be a family of $A$-modules indexed by $I$. For each pair $i$, $j$ in $I$ such that $i\le j$, let $\mu_{ij}:M_i\to M_j$ be an A-homomorphism, and suppose that the following axioms are satisfied:\
(1) $\mu_{ii}$ is the identity mapping of $M_i$, for all $i\in I$.\
(2) $\mu_{ik}=\mu_{jk}\circ\mu_{ij}$ whenever $i\le j\le k$.\
Then the modules $M_i$ and homomorphisms $\mu_{ij}$ are said to form a *direct system* $\mathbf{M}=(M_i,\mu_{ij})$ over the directed set $I$.\
We shall construct an $A$-module $M$ called the *direct limit* of the direct system $\mathbf{M}$. Let $C$ be the direct sum of the $M_i$, and identify each module $M_i$ with its canonical image in $C$. Let $D$ be the submodule of $C$ generated by all elements of the form $x_i-\mu_{ij}(x_i)$, where $i\le j$ and $x_i\in M_i$. Let $M=C/D$, let $\mu:C\to M$ be the projection and let $\mu_i$ be the restriction of $\mu$ to $M_i$.\
The module $M$, or more correctly the pair consisting of $M$ and the family of homomorphisms $\mu_i:M_i\to M$, is called the *direct limit* of the direct system $\mathbf{M}$, and is written $\varinjlim M_i$. From the construction it is clear that $\mu_i=\mu_j\circ\mu_{ij}$ whenever $i\le j$.
{{</exercise>}}

{{<exercise 15>}}
In the situation of Exercise 14, show that every element of $M$ can be written in the form $\mu_i(x_i)$ for some $i\in I$ and some $x_i\in M_i$.
QUESTIONANDANSWERSTRING\
For any preimage $(m_i)$ in $\bigoplus M_i$ there are only finitely many nonzero terms; take the common upper bound $i_0$ of their indices, hence the element is of the form $\mu_{i_0}(\sum\mu_{i,i_0}(m_i))$.
TOMANDJERRYSTRINGLITERAL\
Show also that if $\mu_i(x_i)=0$ in $M$ then there exists $j\ge i$ such that $\mu_{ij}(x_i)=0$ in $M_j$.
QUESTIONANDANSWERSTRING\
If $\mu_i(x_i)=0$, then $x_i$ (in $\bigoplus M_i$) is in $D$, hence a finite linear combination of $x_{j}-\mu_{jk}(x_j)$; taking the upper bound of all involved indices suffices.
{{</exercise>}}

{{<exercise 16>}}
Show that the direct limit is characterized (up to isomorphism) by the following property. Let $N$ be an $A$-module and for each $i\in I$ let $\alpha_i:M_i\to N$ be n $A$-module homomorphism such that $\alpha_i=\alpha_j\circ\mu_{ij}$ whenever $i\le j$. Then there exists a unique homomorphism $\alpha:M\to N$ such that $\alpha_i=\alpha\circ\mu_i$ for all $i\in I$.
{{</exercise>}}

{{<exercise 17>}}
Let $(M_i)_{i\in I}$ be a family of submodules of an $A$-module, such that for each pair of indices $i$, $j$ in $I$ there exists $k\in I$ such that $M_i+M_j\subseteq M_k$. Define $i\le j$ to mean $M_i\subseteq M_j$ and let $\mu_{ij}:M_i\to M_j$ be the embedding of $M_i$ in $M_j$. Show that \[\varinjlim M_i=\sum M_i=\bigcup M_i\]
QUESTIONANDANSWERSTRING\
Consider the map \[\phi:\bigoplus M_i\xrightarrow{(m_i)\mapsto\sum m_i}\sum M_i\] then it is obvious that $D\subseteq\ker(\phi)$; for $(m_i)\in\ker(\phi)$, by taking upper bound of nonzero terms' indices we know that it is a sum of the generators of $D$, hence $\ker(\phi)\subseteq D$. Thus $\phi$ induces an isomorphism $M=C/D\to\sum M_i$.
{{</exercise>}}

{{<exercise 18>}}
Let $\mathbf{M}=(M_i,\mu_{ij})$, $\mathbf{N}=(N_i,\nu_{ij})$ be direct systems of $A$-modules over the same directed set. Let $M$, $N$ be the direct limits and $\mu_i:M_i\to M$, $\nu_i:N_i\to N$ the associated homomorphisms.\
A *homomorphism* $\Phi:\mathbf{M}\to\mathbf{N}$ is by definition a family of $A$-module homomorphisms $\phi_i:M_i\to N_i$ such that $\phi_j\circ\mu_{ij}=\nu_{ij}\circ\phi_i$ whenever $i\le j$. Show that $\Phi$ defines a unique homomorphism $\phi=\varinjlim\phi_i:M\to N$ such that $\phi\circ\mu_i=\nu_i\circ\phi_i$ for all $i\in I$.
{{</exercise>}}

{{<exercise 19>}}
A sequence of direct systems and homomorphisms \[\mathbf{M}\to\mathbf{N}\to\mathbf{P}\] is *exact* if the corresponding sequence of modules and module homomorphisms is exact for each $i\in I$. Show that the sequence $M\to N\to P$ of direct limits is then exact. [Use Exercise 15.]
{{</exercise>}}

### *Tensor Products commute with direct limits* {{<explain>}}Again, see 李文威《代数学方法（卷一）》for more details.{{</explain>}}

{{<exercise 20>}}
Keeping the same notation as in Exercise 14, let $N$ be any $A$-module. Then $(M_i\otimes N,\mu_{ij}\otimes1)$ is a direct system; let $P=\varinjlim(M_i\otimes N)$ be its direct limit. For each $i\in I$ we have a homomorphism $\mu_i\otimes 1:M_i\otimes N\to M\otimes N$, hence by Exercise 16 a homomorphism $\psi:P\to M\otimes N$. Show that $\psi$ is an isomorphism, so that \[\varinjlim(M_i\otimes N)\simeq(\varinjlim M_i)\otimes N\]
[For each $i\in I$, let $g_i:M_i\times N\to M_i\otimes N$ be the canonical bilinear mapping. Passing to the limit we obtain a mapping $g:M\times N\to P$. Show that $g$ is $A$-bilinear and hence define a homomorphism $\phi:M\otimes N\to P$. Verify that $\phi\circ\psi$ and $\psi\circ\phi$ are identity mappings.]
QUESTIONANDANSWERSTRING\
Tensor has Hom as right adjoint, hence preserves all injective limits.
{{</exercise>}}

{{<exercise 21>}}
Let $(A_i)_{i\in I}$ be a family of rings indexed by a directed set $I$, and for each pair $i\le j$ in $I$ let $\alpha_{ij}:A_i\to A_j$ be a ring homomorphism, satisfying conditions (1) and (2) of Exercise 14. Regarding each $A_i$ as a $\mathbf{Z}$-module we can then form the direct limit $A=\varinjlim A_i$. Show that $A$ inherits a ring structure from the $A_i$  so that the mappings $A_i\to $ are ring homomorphisms. The ring $A$ is the *direct limit* of the system $(A_i,\alpha_{ij})$.\
If $A=0$ prove that $A_i=0$ for some $i\in I$. [Remember that all rings have identity elements!]
QUESTIONANDANSWERSTRING\
By Exercise 15 there is some $j$ such that $1_j=\mu_{ij}(1_i)=0_j$.
{{</exercise>}}

{{<exercise 22>}}
Let $(A_i,\alpha_{ij})$ be a direct system of rings and let $\mathfrak{N}_i$ be the nilradical of $A_i$. Show that $\varinjlim \mathfrak{N}_i$ is the nilradical of $\varinjlim A_i$.
QUESTIONANDANSWERSTRING\
By Exercise 15, $\mu_i(x_i)$ nilpotent is equivalent to $\exists j, \mu_{ij}(x_i^n)=0$, i.e., $\mu_i(x_i)=\mu_j(\mu_{ij}(x_i))\in \mu_j(\mathfrak{N}_j)$. The conclusion follows.
TOMANDJERRYSTRINGLITERAL\
If each $A_i$ is an integral domain, then $\varinjlim A_i$ is an integral domain.
QUESTIONANDANSWERSTRING\
Similarly, every equation $xy=0$ in the limit is captured by some large enough indexed $A_j$.
{{</exercise>}}

{{<exercise 23>}}
Let $(B_\lambda)_{\lambda\in\Lambda}$ be a family of $A$-algebras. For each finite subset of $\Lambda$ let $B_J$ denote the tensor product (over $A$) of the $B_\lambda$ for $\lambda\in J$. If $J'$ is another finite subset of $\Lambda$ and $J\subseteq J'$, there is a canonical $A$-algebra homomorphism $B_J\to B_{J'}$. Let $B$ denote the direct limit of the rings $B_J$ as $J$ runs through all finite subsets of $\Lambda$. The ring $B$ has a natural $A$-algebra structure for which the homomorphisms $B_J\to B$ are $A$-algebra homomorphisms. The $A$-algebra $B$ is the *tensor product* of the family $(B_\lambda)$.
{{</exercise>}}

### *Flatness and Tor*
In these Exercises it will be assumed that the reader is familiar with the definition and basic properties of the Tor functor. 
{{<explain>}}The basic properties are:
i) It is additive, $\operatorname{Tor}_0(A,B)=A\otimes B)$, and $\operatorname{Tor}_{<0}(A,B)=0$;
ii) For exact sequence $0\to N'\to N\to N''\to 0$, there is a long exact sequence $\cdots\to\operatorname{Tor}_{n+1}(M,N'')\to\operatorname{Tor}_n(M,N')\to\operatorname{Tor}_n(M,N)\to\operatorname{Tor}_{n-1}(M,N')\to\cdots$ and the same for the second variable;
iii) Take projective resolution (i.e. long exact sequence $\cdots\to P_1\to P_0\to M\to 0$ with each $P_i$ projective) of $M$, then $\operatorname{Tor}_n(M, N) = H[ P_{n+1} \otimes N \to P_{n} \otimes N \to P_{n-1} \otimes N ]$, the $n$-th homology group;
iv) Taking flat resolution (i.e. each $P_i$ flat) of $M$, or similar resolution for $N$, yields the same result;
v) Because we only consider commutative rings with $1$, $\operatorname{Tor}_n(M, N) =\operatorname{Tor}_n(N, M)$.
{{</explain>}}

{{<exercise 24>}}
If $M$ is an $A$-module, the following are equivalent:\
i) $M$ is flat;\
ii) $\operatorname{Tor}_n^A(M,N)=0$ for all $n> 0$ and all $A$-modules $N$;\
ii) $\operatorname{Tor}_1^A(M,N)=0$ for all $A$-modules $N$.\
[To show that (i) $\Rightarrow$ (ii), take a free resolution of $N$ and tensor it with $M$. Since $M$ is flat, the resulting sequence is exact and therefore its homology groups, which are the $\operatorname{Tor}_n^A(M,N)$, are zero for $n> 0$. To show that (iii) $\Rightarrow$ (i), let $0\to N'\to N\to N''\to 0$ be an exact sequence. Then, from the $\operatorname{Tor}$ exact sequence, \[\operatorname{Tor}_1(M,N')\to M\otimes N'\to M\otimes N\to M\otimes N''\to0\] is exact. Since $\operatorname{Tor}_1(M,N')=0$ it follows that $M$ is flat.] {{<explain>}}The hint is exactly the answer.{{</explain>}}
{{</exercise>}}

{{<exercise 25>}}
Let $0\to N'\to N\to N''\to 0$ be an exact sequence, with $N''$ flat. Then $N'$ is flat $\Leftrightarrow N$ is flat. [Use Exercise 24 and the $\operatorname{Tor}$ exact sequence.]
QUESTIONANDANSWERSTRING\
The $\operatorname{Tor}$ exact sequence gives \[\operatorname{Tor}_{n+1}(N'',M)\to \operatorname{Tor}_{n}(N', M)\to\operatorname{Tor}_{n}(N, M)\to\operatorname{Tor}_{n}(N'', M)\] flatness of $N''$ means that both ends are 0, hence the middle terms are isomorphic, i.e. $N$ flat $\Leftrightarrow N'$ flat.
{{</exercise>}}

{{<exercise 26>}}
Let $N$ be an $A$-module. Then $N$ is flat $\Leftrightarrow \operatorname{Tor}_1(A/\mathfrak{a},N)=0$ for all finitely generated ideals $\mathfrak{a}$ in $A$.\
[Show first that $N$ is flat if $\operatorname{Tor}_1(M, N)=0$ for all *finitely generated* $A$-modules $M$, by using (2.19). If $M$ is finitely generated, let $x_1,\ldots,x_n$ be a set of generators of $M$, and let $M_i$ be the submodule generated by $x_1,\ldots,x_i$. By considering the successive quotients $M_i/M_{i-1}$ and using Exercise 25, deduce that $N$ is flat if $\operatorname{Tor}_1(M,N)=0$ for all *cyclic* $A$-modules $M$, i.e., all $M$ generated by a single element, and therefore of the form $A/\mathfrak{a}$ for some ideal $\mathfrak{a}$. Finally use (2.19) again to reduce to the case where $\mathfrak{a}$ is a finitely generated ideal.]
QUESTIONANDANSWERSTRING\
We need a lemma for the sake of convenience: For a direct system $(M_i,\mu_{ij})$, we have \[\operatorname{Tor}_n^A(\varinjlim M_i,N)\simeq \varinjlim\operatorname{Tor}_n^A(M,N)\] this lemma is purely because $\varinjlim$ commutes with tensor products and is exact (hence preserves homology groups).\
Back to the original question, in view of Exercise 24 we only need to prove $\Leftarrow$: for any ideal $\mathfrak{a}$ we have \[A/\mathfrak{a}\simeq\varinjlim_{\substack{\text{finitely generated}\\\text{ideal }\mathfrak{a}'\subseteq\mathfrak{a}}}A/\mathfrak{a}'\] hence by the lemma $\operatorname{Tor}_1^A(M,N)=0$ for each cyclic module $M$. Following the hint, by Exercise 25 and considering successive quotients we know that $\operatorname{Tor}_1^A(M,N)=0$ for all finitely generated $M$. Finally, every module is the $\varinjlim$ of its finitely generated submodules, hence by the lemma again we have $\operatorname{Tor}_1^A(M,N)=0$ for all $M$, i.e. $N$ is flat.
{{</exercise>}}

{{<exercise 27>}}
A ring $A$ is *absolutely flat* if every $A$-module is flat. Prove that the following are equivalent:\
i) $A$ is absolutely flat;\
ii) Every principal ideal is idempotent;\
iii) Every finitely generated ideal is a direct summand of $A$.\
[i) $\Rightarrow$ ii). Let $x\in A$. Then $A/(x)$ is a flat $A$-module, hence in the diagram {{<image 200 90>}}AMimg/AM2_1.svg{{</image>}} the mapping $\alpha$ is injective. Hence $\operatorname{im}(\beta)=0$, hence $(x)=(x)^2$. ii) $\Rightarrow$ iii). Let $x\in A$. Then $x=ax^2$ for some $a\in A$, hence $e=ax$ is idempotent and we have $(e)=(x)$. Now if $e$, $f$ are idempotents, then $(e,f)=(e+f-ef)$. Hence every finitely generated ideal is principal, and generated by an idempotent $e$, hence is a direct summand because $A=(e)\oplus(1-e)$. iii) $\Rightarrow$ i). Use the criterion of Exercise 26.]
QUESTIONANDANSWERSTRING\
The hint basically is the answer. In i) $\Rightarrow$ ii) note that $\alpha$ is induced by $(x)\to A$, which is injective, and also $\alpha\beta=0$; $\operatorname{im}(\beta)=0$ means $(x)/(x^2)=0$. iii) $\Rightarrow$ i) also uses Exercise 4.
{{</exercise>}}

{{<exercise 28>}}
A Boolean ring is absolutely flat.
QUESTIONANDANSWERSTRING\
Every element is idempotent, let alone principal ideals.
TOMANDJERRYSTRINGLITERAL\
The ring of Chapter 1, Exercise 7 is absolutely flat.
QUESTIONANDANSWERSTRING\
$x=x^{n-2}(x^2)\in(x^2)$, hence $(x)=(x^2)$.
TOMANDJERRYSTRINGLITERAL\
Every homomorphic image of an absolutely flat ring is absolutely flat.
QUESTIONANDANSWERSTRING\
Taking quotients does not change ii) in Exercise 27.
TOMANDJERRYSTRINGLITERAL\
If a local ring is absolutely flat, then it is a field.
QUESTIONANDANSWERSTRING\
By Chapter 1, Exercise 12, the idempotents in a local ring must be 0 or 1, i.e. $(x)=(0)$ or $(1)$ for any $x$; this means non-zero elements are all units, hence it is a field.
TOMANDJERRYSTRINGLITERAL\
If $A$ is absolutely flat, every non-unit in $A$ is a zero-divisor.
QUESTIONANDANSWERSTRING\
For non-unit $x$ we have $x\in (x^2)$, i.e. $x(1-ax)=0$ for some $a$. The second term is not 0.
{{</exercise>}}

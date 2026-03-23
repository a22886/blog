+++
date = '2026-02-10T21:46:12+08:00'
title = "4. Primary Decomposition"
categories = ["交换代数"]
series = ["Solutions to Atiyah-MacDonald Commutative Algebra"]
+++

You may want to see [this](../am0/) for unclear notations.

---

{{<exercise 1>}}
If an ideal $\mathfrak{a}$ has a primary decomposition, then $\operatorname{Spec}(A/\mathfrak{a})$ has only finitely many irreducible components.
QUESTIONANDANSWERSTRING\
By Chapter 1, Exercise 20 iii), the irreducible components of $\operatorname{Spec}(A/\mathfrak{a})$ corresponds to the minimal prime ideals $\mathfrak{p}$ among those containing $\mathfrak{a}$. Let $\mathfrak{a}=\bigcap\limits_{i=1}^n\mathfrak{q}_i$ be a primary decomposition, with $\mathfrak{p}_i=r(\mathfrak{q}_i)$, by taking radicals we see $\mathfrak{p}\supseteq \bigcap\limits_{i=1}^n\mathfrak{p}_i$, hence $\mathfrak{p}\supseteq\mathfrak{p}_i$ for some $i$ {{<explain>}}Proposition 1.11{{</explain>}}, by minimality $\mathfrak{p}$ must be one of the $\mathfrak{p}_i$, which provides only a finite number of choices.
{{</exercise>}}

{{<exercise 2>}}
If $\mathfrak{a}=r(\mathfrak{a})$, then $\mathfrak{a}$ has no embedded prime ideals.
QUESTIONANDANSWERSTRING\
If there is an embedded ideal, then taking radical of a minimal primary decomposition of $\mathfrak{a}$ yields another primary decomposition with possibly less terms, contradiction.
{{</exercise>}}

{{<exercise 3>}}
If $A$ is absolutely flat, every primary ideal is maximal.
QUESTIONANDANSWERSTRING\
Passing to quotients we must prove that if an absolutely flat {{<explain>}}The quotient is absolutely flat by Chapter 2, Exercise 28.{{</explain>}} ring $B$'s zero divisors are all nilpotent, then it is a field. But its non-zero-divisors are all units {{<explain>}}Chapter 2, Exercise 28{{</explain>}}, by Proposition 1.6 i) with the ideal $\mathfrak{N}_B$ we know $B$ is local, while Chapter 2, Exercise 28 also tells us that absolutely flat local rings are fields.
{{</exercise>}}

{{<exercise 4>}}
In the polynomial ring $\mathbf{Z}[t]$, the ideal $\mathfrak{m}=(2,t)$ is maximal and the ideal $\mathfrak{q}=(4,t)$ is $\mathfrak{m}$-primary, but is not a power of $\mathfrak{m}$.
QUESTIONANDANSWERSTRING\
Notice $\mathbf{Z}[t]/\mathfrak{m}\simeq\mathbf{Z}_2,\mathbf{Z}[t]/\mathfrak{q}\simeq\mathbf{Z}_4,\mathfrak{m}^2\subsetneq\mathfrak{q}\subsetneq\mathfrak{m}$.
{{</exercise>}}

{{<exercise 5>}}
In the polynomial ring $K[x,y,z]$ where $K$ is a field and $x,y,z$ are independent indeterminates, let $\mathfrak{p}_1=(x,y),\mathfrak{p}_2=(x,z),\mathfrak{m}=(x,y,z)$; $\mathfrak{p}_1$ and $\mathfrak{p}_2$ are prime, and $\mathfrak{m}$ is maximal. Let $\mathfrak{a}=\mathfrak{p}_1\mathfrak{p}_2$. Show that $\mathfrak{a}=\mathfrak{p}_1\cap\mathfrak{p}_2\cap\mathfrak{m}^2$ is a reduced primary decomposition of $\mathfrak{a}$. Which components are isolated and which are embedded?
QUESTIONANDANSWERSTRING\
$\mathfrak{m}^2$ is primary by Proposition 4.2. Once this is indeed a primary decomposition, then $\mathfrak{p}_1$ and $\mathfrak{p}_2$ are the isolated components and $\mathfrak{m}^2$ is the embedded component.\
For $f\in\mathfrak{m}^2$, we can express it as $f=ax^2+by^2+cz^2+dxy+eyz+gzx$; hence $f\in\mathfrak{p}_1\cap\mathfrak{p}_2\Leftrightarrow f\in(x^2,xy,xz,yz)=\mathfrak{a}$, i.e. $\mathfrak{a}=\mathfrak{p}_1\cap\mathfrak{p}_2\cap\mathfrak{m}^2$.
{{</exercise>}}

{{<exercise 6>}}
Let $X$ be an infinite compact Hausdorff space, $C(X)$ the ring of real-valued continuous functions on $X$ (Chapter 1, Exercise 26). Is the zero ideal decomposable in this ring?
QUESTIONANDANSWERSTRING\
No.\
First of all, the maximal ideals of $C(X)$ are $\mathfrak{m}_x$ {{<explain>}}Chapter 1, Exercise 26{{</explain>}}, at which the localization of $C(X)$ is evidently $\mathbf{R}$, hence by Chapter 3, Exercise 10 ii) we see $C(X)$ is absolutely flat, by Exercise 3 every primary ideal is maximal.\
If $(0)=\bigcap\limits_{i=1}^n\mathfrak{m}_{x_i}$, then any function taking $0$ on $x_i$ must be identically zero. By cardinality there must be another point $x$, by Urysohn's lemma there is a function taking $0$ on $x_i$ and $1$ on $x$, contradiction.
{{</exercise>}}

{{<exercise 7>}}
Let $A$ be a ring and let $A[x]$ denote the ring of polynomials in one indeterminate over $A$. For each ideal $\mathfrak{a}$ of $A$, let $\mathfrak{a}[x]$ denote the set of all polynomials in $A[x]$ with coefficients in $\mathfrak{a}$.
TOMANDJERRYSTRINGLITERAL\
i) $\mathfrak{a}[x]$ is the extension of $\mathfrak{a}$ to $A[x]$.
QUESTIONANDANSWERSTRING\
$\mathfrak{a}[x]=\mathfrak{a}\cdot A[x]$.
TOMANDJERRYSTRINGLITERAL\
ii) If $\mathfrak{p}$ is a prime ideal in $A$, then $\mathfrak{p}[x]$ is a prime ideal in $A[x]$.
QUESTIONANDANSWERSTRING\
$A[x]/\mathfrak{p}[x]\simeq(A/\mathfrak{p})[x]$, by Chapter 1, Exercise 2 iii) the polynomial ring on an integral domain is also integral.
TOMANDJERRYSTRINGLITERAL\
iii) If $\mathfrak{q}$ is a $\mathfrak{p}$-primary ideal in $A$, then $\mathfrak{q}[x]$ is a $\mathfrak{p}[x]$-primary ideal in $A[x]$. [Use Chapter 1, Exercise 2.]
QUESTIONANDANSWERSTRING\
By Chapter 1, Exercise 2 ii) and iii), $\mathfrak{q}[x]$ is evidently primary. Under the homomorphism $A[x]\to A[x]/\mathfrak{q}[x]\simeq(A/\mathfrak{q})[x]$, we have \[r(\mathfrak{q}[x])=(\mathfrak{N}_{(A/\mathfrak{q})[x]})^c=(\mathfrak{N}_{A/\mathfrak{q}}[x])^c=(\mathfrak{N}_{A/\mathfrak{q}})^c[x]=\mathfrak{p}[x]\] where the fourth equality is by Chapter 1, Exercise 2 ii).
TOMANDJERRYSTRINGLITERAL\
iv) If $\mathfrak{a}=\bigcap\limits_{i=1}^n\mathfrak{q}_i$ is a minimal primary decomposition in $A$, then $\mathfrak{a}[x]=\bigcap\limits_{i=1}^n\mathfrak{q}_i[x]$ is a minimal primary decomposition in $A[x]$.
QUESTIONANDANSWERSTRING\
Obvious.
TOMANDJERRYSTRINGLITERAL\
v) If $\mathfrak{p}$ is a minimal prime ideal of $\mathfrak{a}$, then $\mathfrak{p}[x]$ is a minimal prime ideal of $\mathfrak{a}[x]$.
QUESTIONANDANSWERSTRING\
Also obvious.
{{</exercise>}}

{{<exercise 8>}}
Let $k$ be a field. Show that in the polynomial ring $k[x_1,\ldots,x_n]$ the ideals $\mathfrak{p}_i=(x_1,\ldots,x_i)~(1\le i\le n)$ are prime and all their powers are primary. [Use Exercise 7.]
QUESTIONANDANSWERSTRING\
$k[x_1,\ldots,x_n]/\mathfrak{p}_i\simeq k[x_{i+1},\ldots,x_n]$ is an integral domain, hence $\mathfrak{p}_i$ is prime. The zero divisors of $k[x_1,\ldots,x_n]/\mathfrak{p}_i^m$ must only involve $x_1,\ldots,x_i$, hence are nilpotent, i.e. $\mathfrak{p}_i^m$ is primary.
{{</exercise>}}

{{<exercise 9>}}
In a ring $A$, let $D(A)$ denote the set of prime ideals $\mathfrak{p}$ which satisfy the following condition: there exists $a\in A$ such that $\mathfrak{p}$ is minimal in the set of prime ideals containing $(0:a)$. Show that $x\in A$ is a zero divisor $\Leftrightarrow x\in\mathfrak{p}$ for some $\mathfrak{p}\in D(A)$.
QUESTIONANDANSWERSTRING\
For $x\in D_A$ {{<explain>}}The set of zero divisors of $A${{</explain>}} take $0\neq y\in (0:x)$, the minimal prime containing $(0:y)$ {{<explain>}}whose existence is guaranteed by Zorn's lemma{{</explain>}} contains $x$. On the other hand we prove every $\mathfrak{p}\in D(A)$ is contained in $D_A$; each such $\mathfrak{p}$ corresponds to a minimal prime $\mathfrak{p}'$ of $A/(0:a)$, which is contained in $D_{A/(0:a)}$ by Chapter 3, Exercise 9, hence by lifting back to $A$ we see every element of $\mathfrak{p}$ is a zero divisor.
TOMANDJERRYSTRINGLITERAL\
Let $S$ be a multiplicatively closed subset of $A$, and identify $\operatorname{Spec}(S^{-1}A)$ with its image in $\operatorname{Spec}(A)$ (Chapter 3, Exercise 21). Show that \[D(S^{-1}A)=D(A)\cap \operatorname{Spec}(S^{-1}A)\]
QUESTIONANDANSWERSTRING\
Rewrite $(0:a)$ as $(0:(a))$ and notice $(0:S^{-1}a)=S^{-1}(0:a)$ {{<explain>}}Proposition 3.14{{</explain>}}, the rest is the prime ideal correspondence provided by $S^{-1}$.
TOMANDJERRYSTRINGLITERAL\
If the zero ideal has a primary decomposition, show that $D(A)$ is the set of associated prime ideals of $0$.
QUESTIONANDANSWERSTRING\
Let $(0)=\bigcap\limits_{i=1}^n\mathfrak{q}_i$ be a reduced primary decomposition with $\mathfrak{p}_i=r(\mathfrak{q}_i)$, for $a\in A$ we have $r(0:a)=\bigcap\limits_{a\not\in\mathfrak{q}_i}\mathfrak{p}_i$. The prime ideals containing $(0:a)$ must contain $r(0:a)$ hence one of $\mathfrak{p}_i$ {{<explain>}}Proposition 1.11{{</explain>}}, thus minimal such primes can only be one of $\mathfrak{p}_i$. Theorem 4.5 taking $\mathfrak{a}=(0)$ says that every $\mathfrak{p}_i$ are indeed in $D(A)$.
{{</exercise>}}

{{<exercise 10>}}
For any prime ideal $\mathfrak{p}$ in a ring $A$, let $S_\mathfrak{p}(0)$ denote the kernel of the homomorphism $A\to A_\mathfrak{p}$. Prove that
TOMANDJERRYSTRINGLITERAL\
i) $S_\mathfrak{p}(0)\subseteq\mathfrak{p}$.
QUESTIONANDANSWERSTRING\
$x\in S_\mathfrak{p}(0)\Leftrightarrow\exists a\in A\backslash\mathfrak{p},ax=0\Rightarrow x\in\mathfrak{p}$.
TOMANDJERRYSTRINGLITERAL\
ii) $r(S_\mathfrak{p}(0))=\mathfrak{p}\Leftrightarrow \mathfrak{p}$ is a minimal prime ideal of $A$.
QUESTIONANDANSWERSTRING\
By Chapter 1, Exercise 18 we have $r(S_\mathfrak{p}(0))=r((0)^c)=(\mathfrak{N}_{A_\mathfrak{p}})^c$, hence $r(S_\mathfrak{p}(0))=\mathfrak{p}\Leftrightarrow\mathfrak{N}_{A_\mathfrak{p}}=\mathfrak{p}_\mathfrak{p}$, i.e. $\mathfrak{p}_\mathfrak{p}$ is the only prime ideal in $A_\mathfrak{p}$, which by prime ideal correspondence means $\mathfrak{p}$ is minimal in $A$.
TOMANDJERRYSTRINGLITERAL\
iii) If $\mathfrak{p}\supseteq\mathfrak{p}'$, then $S_\mathfrak{p}(0)\subseteq S_{\mathfrak{p}'}(0)$.
QUESTIONANDANSWERSTRING\
Because $A\to A_{\mathfrak{p}'}$ factors through $A_\mathfrak{p}$.
TOMANDJERRYSTRINGLITERAL\
iv) $\bigcap\limits_{\mathfrak{p}\in D(A)}S_\mathfrak{p}(0)=0$, where $D(A)$ is defined in Exercise 9.
QUESTIONANDANSWERSTRING\
For any $x\neq 0$ the minimal prime $\mathfrak{p}$ containing $(0:x)$ is in $D(A)$, but $x\not\in S_\mathfrak{p}(0)$.
{{</exercise>}}

{{<exercise 11>}}
If $\mathfrak{p}$ is a minimal prime ideal of a ring $A$, show that $S_\mathfrak{p}(0)$ (Exercise 10) is the smallest $\mathfrak{p}$-primary ideal.
QUESTIONANDANSWERSTRING\
The zero divisors of $A_\mathfrak{p}\supseteq A/S_\mathfrak{p}(0)$ are all nilpotent because $A_\mathfrak{p}$ has only one prime ideal, hence $S_\mathfrak{p}(0)$ is primary. Exercise 10 ii) tells us that it is $\mathfrak{p}$-primary.\
For any $\mathfrak{p}$-primary ideal $\mathfrak{q}$ we have $0\in\mathfrak{q}$ hence $S_\mathfrak{p}(0)=\bigcup\limits_{x\not\in\mathfrak{p}}(0:x)\subseteq\mathfrak{q}$.
TOMANDJERRYSTRINGLITERAL\
Let $\mathfrak{a}$ be the intersection of the ideals $S_\mathfrak{p}(0)$ as $\mathfrak{p}$ runs through the minimal prime ideals of $A$. Show that $\mathfrak{a}$ is contained in the nilradical of $A$.
QUESTIONANDANSWERSTRING\
Use Exercise 10 i), notice that the intersection of all minimal prime ideals is the nilradical.
TOMANDJERRYSTRINGLITERAL\
Suppose that the zero ideal is decomposable. Prove that $\mathfrak{a}=0$ if and only if every prime ideal of $0$ is isolated.
QUESTIONANDANSWERSTRING\
Let $(0)=\bigcap\limits_{i=1}^n\mathfrak{q}_i$ be a reduced primary decomposition with $\mathfrak{p}_i=r(\mathfrak{q}_i)$. Proposition 4.6 says that the minimal prime ideals of $A$ are the minimal ones in $\mathfrak{p}_i$, hence $\mathfrak{a}=\bigcap\limits_{\mathfrak{p}_i\text{:isolated}}S_{\mathfrak{p}_i}(0)=\bigcap\limits_{\mathfrak{p}_i\text{:isolated}}\mathfrak{q}_i$. By minimality of the decomposition w get the result.
{{</exercise>}}

{{<exercise 12>}}
Let $A$ be a ring, $S$ a multiplicatively closed subset of $A$. For any ideal $\mathfrak{a}$, let $S(\mathfrak{a})$ denote the contraction of $S^{-1}\mathfrak{a}$ in $A$. The ideal $S(\mathfrak{a})$ is called the *saturation* of $\mathfrak{a}$ with respect to $S$ {{<explain>}}This definition is compatible with the previously defined $S_p(0)$, with $S_p$ being $A\backslash\mathfrak{p}$.{{</explain>}}. Prove that
TOMANDJERRYSTRINGLITERAL\
i) $S(\mathfrak{a})\cap S(\mathfrak{b})=S(\mathfrak{a}\cap\mathfrak{b})$
QUESTIONANDANSWERSTRING\
Chapter 1, Exercise 18.
TOMANDJERRYSTRINGLITERAL\
ii) $S(r(\mathfrak{a}))=r(S(\mathfrak{a}))$
QUESTIONANDANSWERSTRING\
Chapter 1, Exercise 18.
TOMANDJERRYSTRINGLITERAL\
iii) $S(\mathfrak{a})=(1)\Leftrightarrow \mathfrak{a}$ meets $S$
QUESTIONANDANSWERSTRING\
Proposition 3.11.
TOMANDJERRYSTRINGLITERAL\
iv) $S_1(S_2(\mathfrak{a}))=(S_1S_2)(\mathfrak{a})$.
QUESTIONANDANSWERSTRING\
Similar to Chapter 3, Exercise 3; one can also verify by $S(\mathfrak{a})=\bigcup\limits_{s\in S}(\mathfrak{a}:s)$.
TOMANDJERRYSTRINGLITERAL\
If $\mathfrak{a}$ has a primary decomposition, prove that the set of ideals $S(\mathfrak{a})$ (where $S$ runs through all multiplicatively closed subsets of $A$) is finite.
QUESTIONANDANSWERSTRING\
By Proposition 4.9, these ideals can only be intersections of $\mathfrak{q}_i$, which is finite in number.
{{</exercise>}}

{{<exercise 13>}}
Let $A$ be a ring and $\mathfrak{p}$ a prime ideal of $A$. The *$n$th symbolic power of $\mathfrak{p}$* is defined to be the ideal (in the notation of Exercise 12) \[\mathfrak{p}^{(n)}=S_\mathfrak{p}(\mathfrak{p}^n)\]
where $S_\mathfrak{p}=A-\mathfrak{p}$. Show that
TOMANDJERRYSTRINGLITERAL\
i) $\mathfrak{p}^{(n)}$ is a $\mathfrak{p}$-primary ideal;
QUESTIONANDANSWERSTRING\
Use Proposition 4.2 in view of the primary ideal correspondence Proposition 4.8.
TOMANDJERRYSTRINGLITERAL\
ii) if $\mathfrak{p}^n$ has a primary decomposition, then $\mathfrak{p}^{(n)}$ is its $\mathfrak{p}$-primary component.
QUESTIONANDANSWERSTRING\
Let $\mathfrak{p}^n=\bigcap\limits_{i=1}^k\mathfrak{q}_i$ be a minimal primary decomposition with $\mathfrak{p}_i=r(\mathfrak{q}_i)$, then $(\mathfrak{p}_\mathfrak{p})^n=(\mathfrak{p}^n)_\mathfrak{p}=\bigcap\limits_{\mathfrak{q}_i\cap S_\mathfrak{p}=\varnothing}(\mathfrak{q}_i)_\mathfrak{p}$ is a minimal primary decomposition by Proposition 4.9. But itself is primary by Proposition 4.2, hence there is only one $\mathfrak{p}_i\cap S_\mathfrak{p}=\varnothing$ (which is an isolated component) and $\mathfrak{p}_i=r((\mathfrak{p}^n)_\mathfrak{p})^c=r(\mathfrak{p}_\mathfrak{p})^c=\mathfrak{p}$, by taking contraction we see $\mathfrak{q}_i=\mathfrak{p}^{(n)}$.
TOMANDJERRYSTRINGLITERAL\
iii) if $\mathfrak{p}^{(m)}\mathfrak{p}^{(n)}$ has a primary decomposition, then $\mathfrak{p}^{(m+n)}$ is its $\mathfrak{p}$-primary component.
QUESTIONANDANSWERSTRING\
The proof is nearly identical to Exercise 13 ii), in which we consider $(\mathfrak{p}^{(m)}\mathfrak{p}^{(n)})_\mathfrak{p}=(\mathfrak{p}^{(m)}_\mathfrak{p})(\mathfrak{p}^{(n)}_\mathfrak{p})=(\mathfrak{p}_\mathfrak{p})^{m+n}$.
TOMANDJERRYSTRINGLITERAL\
iv) $\mathfrak{p}^{(n)}=\mathfrak{p}^n \Leftrightarrow \mathfrak{p}^{(n)}$ is $\mathfrak{p}$-primary.
QUESTIONANDANSWERSTRING\
The two directions are covered in Exercise 13 i) and ii), in which we consider the primary decomposition $\mathfrak{p}^n=\mathfrak{p}^{(n)}$.
{{</exercise>}}

{{<exercise 14>}}
Let $\mathfrak{a}$ be a decomposable ideal in a ring $A$ and let $\mathfrak{p}$ be a maximal element of the set of ideals $(\mathfrak{a}:x)$, where $x\in A$ and $x\not\in\mathfrak{a}$. Show that $\mathfrak{p}$ is a prime ideal belonging to $\mathfrak{a}$.
QUESTIONANDANSWERSTRING\
Let $\mathfrak{a}=\bigcap\limits_{i=1}^n\mathfrak{q}_i$. Let $\mathfrak{p}=(\mathfrak{a}:x)=\bigcap\limits_{x\not\in\mathfrak{q}_i}(\mathfrak{q}_i:x)$, denote $I=\{i:x\not\in\mathfrak{q}_i\}$, and take a minimal element $\mathfrak{p}_{i_0}$ of $\{r(\mathfrak{q}_i):i\in I\}$. We prove $\mathfrak{p}=\mathfrak{p}_{i_0}$.\
First of all we cannot have $\bigcap\limits_{I\ni j\neq i_0}\mathfrak{q}_j\subseteq\mathfrak{p}_{i_0}$ or else taking radical yields contradiction. Thus we can take $y\in \bigcap\limits_{I\ni j\neq i_0}\mathfrak{q}_j\backslash\mathfrak{p}_{i_0}$. By definition $xy\in \bigcap\limits_{j\neq i_0}\mathfrak{q}_j\backslash\mathfrak{q}_{i_0}$, and now $\mathfrak{p}=(\mathfrak{a}:x)\subseteq(\mathfrak{a}:xy)=(\mathfrak{q}_{i_0}:xy)$. By maximality it must be equality.\
If $(\mathfrak{q}_{i_0}:xy)\neq\mathfrak{p}_{i_0}$, then we can take $u\in(\mathfrak{q}_{i_0}:xy)\backslash\mathfrak{p}_{i_0}$ and minimal $n$ such that $xyu^n\in\mathfrak{q}_{i_0}$, and $(\mathfrak{q}_{i_0}:xy)\subsetneq(\mathfrak{q}_{i_0}:xyu^{n-1})\neq(1)$ contradicts maximality of $\mathfrak{p}$.
{{</exercise>}}

{{<exercise 15>}}
Let $\mathfrak{a}$ be a decomposable ideal in a ring $A$, let $\Sigma$ be an isolated set of prime ideals belonging to $\mathfrak{a}$, and let $\mathfrak{q}_\Sigma$ be the intersection of the corresponding primary components. Let $f$ be a element of $A$ such that, for each prime ideal $\mathfrak{p}$ belonging to $\mathfrak{a}$, we have $f\in \mathfrak{p}\Leftrightarrow\mathfrak{p}\not\in\Sigma$, and let $S_f$ be the set of all powers of $f$. Show that $\mathfrak{q}_\Sigma=S_f(\mathfrak{a})=(\mathfrak{a}:f^n)$ for all large $n$.
QUESTIONANDANSWERSTRING\
By Proposition 4.9 and 3.11, $q_\Sigma=S_f(\mathfrak{a})=\bigcup\limits_{n=0}^{\infty}(\mathfrak{a}:f^n)$. Let $\mathfrak{a}=\bigcap\limits_{i=1}^n\mathfrak{q}_i$ and $r(\mathfrak{q}_i)=\mathfrak{p}_i$, by definition there is some $n$ such that $f^n\in \mathfrak{q}_i$ for all indices $i$ such that $\mathfrak{p}_\not\in\Sigma$, which means $f^nq_\Sigma\subseteq\mathfrak{a}$. This gives the second equality.
{{</exercise>}}

{{<exercise 16>}}
If $A$ is a ring in which every ideal has a primary decomposition, show that every ring of fractions $S^{-1}A$ has the same property.
QUESTIONANDANSWERSTRING\
By Proposition 4.9 and Proposition 3.11 i).
{{</exercise>}}

{{<exercise 17>}}
Let $A$ be a ring with the following property.\
(L1) For every ideal $\mathfrak{a}\neq(1)$ in $A$ and every prime ideal $\mathfrak{p}$, there exists $x\not\in\mathfrak{p}$ such that $S_\mathfrak{p}(\mathfrak{a})=(\mathfrak{a}:x)$, where $S_\mathfrak{p}=A-\mathfrak{p}$.\
Then every ideal in $A$ is an intersection of (possibly infinitely many) primary ideals.\
[Let $\mathfrak{a}$ be an ideal $\neq(1)$ in $A$, and let $\mathfrak{p}_1$ be a minimal element of the set of prime ideals containing $\mathfrak{a}$. Then $\mathfrak{q}_1=S_{\mathfrak{p}_1}(\mathfrak{a})$ is $\mathfrak{p}_1$-primary (by Exercise 11), and $\mathfrak{q}_1=(\mathfrak{a}:x)$ for some $x\not\in\mathfrak{p}_1$. Show that $\mathfrak{a}=\mathfrak{q}_1\cap(\mathfrak{a}+(x))$.\
Now let $\mathfrak{a}_1$ be a maximal element of the set of ideals $\mathfrak{b}\supseteq\mathfrak{a}$ such that $\mathfrak{q}_1\cap\mathfrak{b}=\mathfrak{a}$, and choose $\mathfrak{a}_1$ so that $x\in\mathfrak{a}_1$, and therefore $\mathfrak{a}_1\not\subseteq\mathfrak{p}_1$. Repeat the construction starting with $\mathfrak{a}_1$, and so on. At the $n$th stage we have $\mathfrak{a}=\mathfrak{q}_1\cap\cdots\cap\mathfrak{q}_n\cap\mathfrak{a}_n$ where the $\mathfrak{q}_i$ are primary ideals, $\mathfrak{a}_n$ is maximal among the ideals $\mathfrak{b}$ containing $\mathfrak{a}_{n-1}=\mathfrak{a}_n\cap\mathfrak{q}_n$ such that $\mathfrak{a}=\mathfrak{q}_1\cap\cdots\cap\mathfrak{q}_n\cap\mathfrak{b}$, and $\mathfrak{a}_n\not\subseteq\mathfrak{p}_n$. If at any stage we have $\mathfrak{a}_n=(1)$, the process stops, and $\mathfrak{a}$ is a finite intersection of primary ideals. If not, continue by transfinite induction, observing that each $\mathfrak{a}_n$ strictly contains $\mathfrak{a}_{n-1}$.] {{<explain>}}The hint is exactly the answer.{{</explain>}}
{{</exercise>}}

{{<exercise 18>}}
Consider the following condition on a ring $A$:\
(L2) Given an ideal $\mathfrak{a}$ and a descending chain $S_1\supseteq S_2\supseteq\cdots\supseteq S_n\supseteq\cdots$ of multiplicatively closed subsets of $A$, there exists an integer $n$ such that $S_n(\mathfrak{a})=S_{n+1}(\mathfrak{a})=\cdots$. Prove that the following are equivalent:\
i) Every ideal in $A$ has a primary decomposition.\
ii) $A$ satisfies (L1) and (L2).\
[For i) $\Rightarrow$ ii), use Exercises 12 and 15. For ii) $\Rightarrow$ i) show, with the notation of the proof of Exercise 17, that if $S_n=S_{\mathfrak{p}_1}\cap\cdots\cap S_{\mathfrak{p}_n}$ then $S_n$ meets $\mathfrak{a}_n$, hence $S_n(\mathfrak{a}_n)=(1)$, and therefore $S_n(\mathfrak{a})=\mathfrak{q}_1\cap\cdots\cap\mathfrak{q}_n$. Now use (L2) to show that the construction must terminate after a finite number of steps.]
QUESTIONANDANSWERSTRING\
For i) $\Rightarrow$ ii), Exercise 12 implies (L2); let $\mathfrak{a}=\bigcap\limits_{i=1}^n\mathfrak{q}_i$, then $S_\mathfrak{p}(\mathfrak{a})=\bigcap\limits_{r(\mathfrak{q}_i)\subseteq\mathfrak{p}}\mathfrak{q}_i=\bigcap\limits_{\mathfrak{q}_i\subseteq\mathfrak{p}}\mathfrak{q}_i$ by Proposition 4.9. Take one $x_i\in\mathfrak{q}_i\backslash\mathfrak{p}$ for each $\mathfrak{q}_i\not\subseteq\mathfrak{p}$ and make their product $x=\prod x_i$, we have $x\in\mathfrak{q}_i\Leftrightarrow\mathfrak{q}_i\not\subseteq\mathfrak{p}$ for any $i$, thus $(\mathfrak{a}:x)=\bigcap\limits_{\mathfrak{q}_i\subseteq\mathfrak{p}}\mathfrak{q}_i=S_\mathfrak{p}(\mathfrak{a})$.\
For ii) $\Rightarrow$ i), the hint is basically the answer; we use (L2) to show $S_n(\mathfrak{a})$ stabilizes, i.e. there is some $n$ such that $\bigcap\limits_{i=1}^{n-1}\mathfrak{q}_i=\bigcap\limits_{i=1}^{n}\mathfrak{q}_i$. By construction $\mathfrak{a}=\bigcap\limits_{i=1}^{n}\mathfrak{q}_i\cap\mathfrak{a}_{n+1}=\bigcap\limits_{i=1}^{n-1}\mathfrak{q}_i\cap\mathfrak{a}_{n}$ with $\mathfrak{a_n}$ being maximal, hence the construction stops at $\mathfrak{a}_n$ or else $\mathfrak{a}_{n+1}\supsetneq\mathfrak{a}_n$ contradicting maximality.
{{</exercise>}}

{{<exercise 19>}}
Let $A$ be a ring and $\mathfrak{p}$ a prime ideal of $A$. Show that every $\mathfrak{p}$-primary ideal contains $S_\mathfrak{p}(0)$, the kernel of the canonical homomorphism $A\to A_\mathfrak{p}$.
QUESTIONANDANSWERSTRING\
See Exercise 11.
TOMANDJERRYSTRINGLITERAL\
Suppose that $A$ satisfies the following condition: for every prime ideal $\mathfrak{p}$, the intersection of all $\mathfrak{p}$-primary ideals of $A$ is equal to $S_\mathfrak{p}(0)$. (Noetherian rings satisfy this condition: see Chapter 10.) Let $\mathfrak{p}_1,\ldots,\mathfrak{p}_n$ be distinct prime ideals, none of which is a minimal prime ideal of $A$. Then there exists an ideal $\mathfrak{a}$ in $A$ whose associated prime ideals are $\mathfrak{p}_1,\ldots,\mathfrak{p}_n$.\
[Proof by induction on $n$. The case $n=1$ is trivial (take $\mathfrak{a}=\mathfrak{p}_1$). Suppose $n>1$ and let $\mathfrak{p}_n$ be maximal in the set $\{\mathfrak{p}_1,\ldots,\mathfrak{p}_n\}$. By the inductive hypothesis, there exists an ideal $\mathfrak{b}$ and a minimal primary decomposition $\mathfrak{b}=\mathfrak{q}_1\cap\cdots\cap\mathfrak{q}_{n-1}$, where each $\mathfrak{q}_i$ is $\mathfrak{p}_i$-primary. If $\mathfrak{b}\subseteq S_{\mathfrak{p}_n}(0)$, let $\mathfrak{p}$ be a minimal prime ideal of $A$ contained in $\mathfrak{p}_n$. Then $S_{\mathfrak{p}_n}(0)\subseteq S_{\mathfrak{p}}(0)$, hence $\mathfrak{b}\subseteq S_{\mathfrak{p}}(0)$. Taking radicals and using Exercise 10, we have $\mathfrak{p}_1\cap\cdots\cap\mathfrak{p}_{n-1}\subseteq\mathfrak{p}$, hence some $\mathfrak{p}_i\subseteq\mathfrak{p}$, hence $\mathfrak{p}_i=\mathfrak{p}$ since $\mathfrak{p}$ is minimal. This is a contradiction since no $\mathfrak{p}_i$ is minimal. Hence $\mathfrak{b}\not\subseteq S_{\mathfrak{p}_n}(0)$ and therefore there exists a $\mathfrak{p}_n$-primary ideal $\mathfrak{q}_n$ such that $\mathfrak{b}\not\subseteq\mathfrak{q}_n$. Show that $\mathfrak{a}=\mathfrak{q}_1\cap\cdots\cap\mathfrak{q}_n$ has the required properties.]
QUESTIONANDANSWERSTRING\
The last step of the hint only needs proving minimality of the decomposition, which is because if another $1\le i < n$ satisfy $\bigcap\limits_{j\neq i}\mathfrak{q}_j\subseteq\mathfrak{q}_i$, then taking radical on both sides contradicts $\mathfrak{p}_n$'s maximality.
{{</exercise>}}

### *Primary decomposition of modules* 
Practically the whole of this chapter can be transposed to the context of modules over a ring $A$. The following exercises indicate how this is done. {{<explain>}}The proofs are also nearly identical to the case with rings and ideals, so we skip them here.{{</explain>}}

{{<exercise 20>}}
Let $M$ be a fixed $A$-module, $N$ a submodule of $M$. The *radical* of $N$ in $M$ is defined to be \[r_M(N)=\{x\in A:x^qM\subseteq N\text{ for some }q>0\}.\]
Show that $r_M(N)=r(N:M)=r(\operatorname{Ann}(M/N))$. In particular, $r_M(N)$ is an *ideal*.\
State and prove the formulas for $r_M$ analogous to (1.13).
{{</exercise>}}

{{<exercise 21>}}
An element $x\in A$ defines an endomorphism $\phi_x$ of $M$, namely $m\mapsto xm$. The element $x$ is said to be a *zero-divisor* (resp. *nilpotent*) *in* $M$ if $\phi_x$ is not injective (resp. is nilpotent). A submodule $Q$ of $M$ is *primary in* $M$ if $Q\neq M$ and every zero-divisor in $M/Q$ is nilpotent.\
Show that if $Q$ is primary in $M$, then $(Q:M)$ is a primary ideal and hence $r_M(Q)$ is a prime ideal $\mathfrak{p}$. We say that $Q$ is $\mathfrak{p}$-*primary* (in $M$).\
Prove the analogues of (4.3) and (4.4).
{{</exercise>}}

{{<exercise 22>}}
A *primary decomposition of $N$ in $M$* is a representation of $N$ as an intersection \[N=Q_1\cap\cdots\cap Q_n\] of primary submodules of $M$; it is a *minimal primary decomposition* if the ideals $\mathfrak{p}_i=r_M(Q_i)$ are all distinct and if none of the components $Q_i$ can be omitted from the intersection, that is if $Q_i\not\supseteq\bigcap\limits_{j\neq i}Q_j~(1\le i\le n)$.\
Prove the analogue of (4.5), that the prime ideals $\mathfrak{p}_i$ depend only on $N$ (and $M$). They are called the *prime ideals belonging to $N$ in $M$*. Show that they are also the prime ideals belonging to 0 in $M/N$.
{{</exercise>}}

{{<exercise 23>}}
State and prove the analogues of (4.6)-(4.11) inclusive. (There is no loss of generality in taking $N=0$.)
{{</exercise>}}

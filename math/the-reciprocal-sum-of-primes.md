Suppose $\sum_{p}{p^{-1}}$ converges. Then there exists a number $N$ so that $\sum_{p>N}{p^{-1}} < 1/2$.

Let $Q=\prod_{p\leq N}p$. Then $1+nQ$ is not divisible by any prime $p \leq N$.

Consider this inequality:

$$
\sum_{n=1}^{\infty}(1+nQ)^{-1} \leq \sum_{k=1}^{\infty}(\sum_{p>N}{p^{-1}})^{k}
$$

This is true, because RHS contains all the terms in LHS.

However, we've chosen $N$ so that  $\sum_{p>N}{p^{-1}} < 1/2$. So RHS is less than equal to $\sum{2^{-k}}=1$.

This is a contradiction since LHS diverges.
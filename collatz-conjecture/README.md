# Collatz Conjecture

This very first article [^1] is interesting.

$$
b_{a}^{p} = \frac{1}{3^p}(b_{a}^{0}\times2^{\sum_{i=0}^{p}n_{i}}-\sum_{i=0}^{p} 3^
{p-i}\times2^{\sum_{j=1}^{i-1}n_{j}})
$$

## The problem


$$
f(n) =
    \begin{cases}
      n/2 & \text{if }n \equiv 0 \mod 2\\
      3n+1 & \text{if }n \equiv 1 \mod 2 
    \end{cases}  
$$

The conjecture

>   This process will eventually reach the number 1, regardless of which positive integer is chosen initially.


## Generator

Any function of the form:

$$
\begin{split}
\mathcal{G} :\ & \mathbb{N} \rightarrow \mathbb{N}\\
   & a \rightarrow a \times 2^p ,p \in \mathbb{N}
\end{split} 
$$

is defined as a generator for the Syracuse problem because any number leading to a function of this form will fall down to $$1$$ after $$n$$ iterations.

Anytime a number $$a$$ is having the following property, the conjecture is demonstrated:

$$
\exists p \in \mathbb{N}, f(a) = 3a + 1 = \mathcal{G}(p)
$$

This means that any number respecting the following equation is validating the conjecture:

$$
a = \frac{\mathcal{G}(p) - 1}{3} = \frac{2^p - 1}{3}
$$

The question is then: is there for any number $$a \in \mathbb{N}$$, a fixed number number of iteration for $$f$$ leading to a generator function?

If this is the case, the conjecture seems to be demonstrated.

### Relation between generators

Does the following relation truth?

$$
\forall b \in m\mathbb{N}, \exists! a \in \mathbb{N} / f(\mathcal{G}_b) = \mathcal{G}_a
$$

---

[^1] [Wikipedia](https://en.wikipedia.org/wiki/Collatz_conjecture)
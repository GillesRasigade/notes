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
      n/2 & \text{if $n \equiv 0 \mod 2$ }\\
      3n+1 & \text{if $n \equiv 1 \mod 2$ }
    \end{cases}  
$$

The conjecture

>   This process will eventually reach the number 1, regardless of which positive integer is chosen initially.


## Generator

Any function of the form:

$$
f_{n} = 2^{n}
$$

is defined as a generator for the Syracuse problem because any number leading to a function of this form will fall down to $$1$$ after $$n$$ iterations


---

[^1] [Wikipedia](https://en.wikipedia.org/wiki/Collatz_conjecture)
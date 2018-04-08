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

> This process will eventually reach the number 1, regardless of which positive integer is chosen initially.

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


The question is then: is there for any number $$a \in \mathbb{N}$$, a fixed number of iteration for $$f$$ leading to a generator function?

If this is the case, the conjecture is demonstrated.

### Relation between generators

> A _generator_ has **several** _children_ but a **single** _parent_.

Is the following relation truth?


$$
\forall b \in \mathbb{N}, \exists! a \in \mathbb{N} / \\
f(\mathcal{G}_b) = \mathcal{G}_a
$$


Demonstration

`Written, must be copied here`

Conclusion

A _generator_ has several children by the application of the function $$f$$ but has a single parent by the application of the same function.

### Neutral element

The _generator_ $$\mathcal{G}_1$$ is a neutral element for the function $$f$$:


$$
f(\mathcal{G}_1) = \mathcal{G}_1
$$


with


$$
\mathcal{G}_1 = 2^p, p \in \mathbb{N}
$$


Questions:

* Do we have other neutral elements for the function $$f$$?
* Is there a relation between neutral elements and cycles for the function $$f$$?

#### Demonstration


$$
\begin{split}
f(\mathcal{G}_a) & = & \mathcal{G} & a \in \mathbb{N} \\
3 \times a 2^p + 1 & = & a 2^q & \implies q > p \\
a\left( 2^q - 3 \times 2^p \right) & = & 1 \\
a 2^p \left( 2^{q-p} - 3 \right) & = & 1 \\
a & = & \frac{1}{2^p \left( 2^{q-p} - 3 \right)} \\
a, p, n \in \mathbb{N} & \implies & a = 1
\end{split}
$$


### Children of a generator

A generator $$\mathcal{G}_a$$ is having the following children by application of the reverse function of $$f$$:


$$
\begin{split}
f^{-1}(\mathcal{G}_a) & = & \frac{a 2^p - 1}{3} \in \mathbb{N}, p \in \mathbb{N} \\
\end{split}
$$


What are the values of $$p$$?

<!--
| $$n$$ | $$2^n$$ | $$1$$ |$$3$$ | $$5$$ | $$7$$ | $$9$$ | $$11$$ | $$13$$ | $$15$$ | $$17$$ | $$19$$ |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
|  $$0$$ | $$1$$ |||||||||||
-->

All odd numbers can be defined with the following form:

$$
a = 3 \left( n \pm 0,2 \right), n \in \mathbb{N^*}
$$

Leading to

$$
1, 3, 5 - 7, 9, 11 - 13, 15, 17 - 19, 21, 23 - 25, 27, 29 - ...
$$

Thus, what are accepted values of $$p$$ with the following form?

$$
\begin{split}
f^{-1}(\mathcal{G}_a) & = & \frac{a 2^p - 1}{3} \in \mathbb{N}, p \in \mathbb{N} \\
& = & \frac{3 \left( n \pm 0,2 \right) 2^p - 1}{3} \in\mathbb{N}, \forall n \in \mathbb{N} 
\end{split}
$$

For $$a = 3n, n \in \mathbb{N}$$

$$
\begin{split}
f^{-1}(\mathcal{G}_a) & = & \frac{a 2^p - 1}{3} \in \mathbb{N}, p \in \mathbb{N} \\
& = & \frac{3 n 2^p - 1}{3} \in\mathbb{N}, \forall n \in \mathbb{N} \\
& = & n2^p - \frac{1}{3} \not\in \mathbb{N}, \forall n, p \in \mathbb{N}
\end{split}
$$

> **Conclusion** A generator of type $$\mathcal{G}_{3k}, k \in \mathbb{N}$$ does not have any children generator.


---

[^1] [Wikipedia](https://en.wikipedia.org/wiki/Collatz_conjecture)


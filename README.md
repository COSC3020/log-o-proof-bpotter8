[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

# Revised Answer:

If we cannot assume a particular T(n), then we must prove that 

$O(log_{2} n) \subseteq O(log_{5} n)$ and $O(log_{5} n) \subseteq O(log_{2} n)$

$log_{2} n$ = $\frac {log_{5} n} {log_{5} 2}$

c = $\frac {1} {log_{5} 2}$

$log_{2} n \leq c \cdot log_{5} n$

$\frac {log_{5} n} {log_{5} 2} \leq \frac {1} {log_{5} 2} \cdot log_{5} n$ (They are equal)

So, $O(log_{2} n) \subseteq O(log_{5} n)$

$log_{5} n$ = $\frac {log_{2} n} {log_{2} 5}$

c = $log_{2} 5$

$log_{5} n \leq c \cdot log_{2} n$

$\frac {log_{2} n} {log_{2} 5} \leq log_{2} 5 \cdot log_{2} n$ (This is always true)

So, $O(log_{5} n) \subseteq O(log_{2} n)$

Because $O(log_{2} n) \subseteq O(log_{5} n)$ and $O(log_{5} n) \subseteq O(log_{2} n)$, 
then it must be true that $O(log_{2} n)$ is the same as $O(log_{5} n)$.

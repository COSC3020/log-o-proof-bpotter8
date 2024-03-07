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

# Answer:

If we cannot assume a particular T(n) or c, then we must prove that 

$O(log_{2} n) \subseteq O(log_{5} n)$ and $O(log_{5} n) \subseteq O(log_{2} n)$

T(n) $\leq c \cdot log_{5} n$

$log_{5} n$ = $\frac {log_{2} n} {log_{2} 5} $

T(n) $\leq c \cdot \frac {log_{2} n} {log_{2} 5}$

T(n) $\leq \frac {c \cdot log_{2} n} {log_{2} 5}$

$log_{2} 5$ is combined with c because they are both constants

T(n) $\leq c \cdot log_{2} n$

If T(n) $\leq c \cdot log_{2} n$ is true, then

$log_{2} n$ = $\frac {log_{5} n} {log_{5} 2} $

T(n) $\leq c \cdot \frac {log_{5} n} {log_{5} 2} $

T(n) $\leq c \cdot log_{5} n$

Because $O(log_{2} n) \subseteq O(log_{5} n)$ and $O(log_{5} n) \subseteq O(log_{2} n)$, 
then it must be true that $O(log_{2} n)$ is the same as $O(log_{5} n)$.

- The knowledge from this article comes from the book 'Design and Analysis of algorithms'

# Divide and Conquer

- typical DnC algorithms have the below structure
  - divide problems into subproblems
  - solve the subproblems (recusive invocation)
  - combine the solution to subproblems

## Time complexity

- And gives rise to the recurrence equation
  - $T(n) = aT(n/b) + \theta(n)$
  - the last theta part
    - can have many other forms
    - is the cost of dividing and combining

### 'Algorithmic'

- for the recurrence to be 'algorithmic'
- The domain where $T(n)$ is defined, the n's should fall down to base cases
- The base cases should be run in constant time
- I guess the authors think only such recurrences are analysable

## Example

- merge sort

## ways to prove time complexity

- Substitution method
- Recurrence tree method
- Master Theorem

## Substitution Proof

- basically proof by induction

### Steps

  $T(n) = aT(n/b) + \theta(n)$

1. State the time complexity that you hope a recurrence equation is bounded by,  like $O(n)$

- and that is a guess
- this means claiming there exist $c$ and $n_0$ such that are positive and $T(n) <= cn$ for $n> n_0$

1. Choose the inductive hypothesis, that it holds for the smaller value in the RHS's $T(n/b)$

- the hypothesis is normally $T(n) <= cn$ but sometimes $T(n) <= cn - d$ for some $d>0$ helps proof

- substitute the hypothesis it, which will make a inequality

  $T(n) = aT(n/b) + \theta(n) <=  a(cn/b) + \theta(n)$

1. and hence proving that the inequality holds for LHS $T(n)$ as well.
1. now prove for base case.

- the base case should be identified

- this seems real vague but different recurrences require different logic
- important to remember that in the end it is Mathematical induction and keep the entire logic streamlines

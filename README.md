# Improved Long Gaps Between Primes

This repository contains a Lean 4 formalization of the results presented in
[Improved Long Gaps Between Primes](https://cdn.openai.com/pdf/51126fac-1b68-4128-9666-c908bcc16033/long_gaps.pdf) by OpenAI.

- [Read the paper](https://cdn.openai.com/pdf/51126fac-1b68-4128-9666-c908bcc16033/long_gaps.pdf)
- [Read the abridged chain of thought](https://cdn.openai.com/pdf/51126fac-1b68-4128-9666-c908bcc16033/long_gaps_abridged_cot.pdf)

## Main result

We prove that, for all sufficiently large $X$,

```math
G(X) \gg \frac{\log\,X\,(\log \; \log\,X)^2\,\log \; \log \; \log \; \log\,X}
             {(\log \; \log \; \log\,X)^2},
```

where $G(X)$ is the largest gap between consecutive primes not exceeding $X$.
Here, $\log$ denotes the natural logarithm and $\gg$ denotes a lower bound
up to a positive multiplicative constant independent of $X$.

## Building the formalization

The project uses Lean 4.33.0, mathlib, and Lake. With
[elan](https://github.com/leanprover/elan) installed, fetch the mathlib cache
and build the formalization with:

```sh
lake exe cache get
lake build
```

## Independent proof checking

Install `landrun`, `lean4export`, and `nanoda_bin`, and make them available on
`PATH`. Then, from the repository root:

```sh
lake exe cache get
lake exe comparator comparator.json
```

# Improved Long Gaps Between Primes

This repository contains a Lean 4 formalization of the results presented in
*Improved Long Gaps Between Primes* by OpenAI.

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


## Fork context

This repository is a fork of [OpenAI/LongGapsBetweenPrimes](https://github.com/openai/LongGapsBetweenPrimes). It is a Lean formalization workspace for an existing published result, not a claim that this fork independently discovered or proved a new theorem. Preserve the upstream attribution and Apache-2.0 licensing terms when redistributing changes.

For mathematical claims, consult the original paper and verify the formalization at the exact commit and toolchain used. A successful Lean build checks the encoded statements; it does not by itself establish that the formalization matches every intended statement in the paper.

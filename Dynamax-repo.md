# Dynamax-repo.md

Note Created: 2024-01-25

source: [probml/dynamax](https://github.com/probml/dynamax)

type: State Space Models

keywords: state-space-models, JAX, kalman-filter, hidden-markov-models

paper: [Probabilistic Machine Learning: Advanced Topics](https://probml.github.io/pml-book/book2.html)

replicated: tooling

papers with code: (${7:paperswithcodeurl})

tasks: prediction (classification and regression), generation(of images or text), discovery (of "meaningful structure" in data) and control (optimal decision making).

## Summary

Dynamax is a library for probabilistic state space models (SSMs) written in JAX. It has code for inference (state estimation) and learning (parameter estimation) in a variety of SSMs, including:

Hidden Markov Models (HMMs)
Linear Gaussian State Space Models (aka Linear Dynamical Systems)
Nonlinear Gaussian State Space Models
Generalized Gaussian State Space Models (with non-Gaussian emission models)
The library consists of a set of core, functionally pure, low-level inference algorithms, as well as a set of model classes which provide a more user-friendly, object-oriented interface. It is compatible with other libraries in the JAX ecosystem, such as optax (used for estimating parameters using stochastic gradient descent), and Blackjax (used for computing the parameter posterior using Hamiltonian Monte Carlo (HMC) or sequential Monte Carlo (SMC)).

Colab notebooks are available.

## Citation
Chapter 29 of:
 @book{pml2Book,
 author = "Kevin P. Murphy",
 title = "Probabilistic Machine Learning: Advanced Topics",
 publisher = "MIT Press",
 year = 2023,
 url = "http://probml.github.io/book2"
}

@book{bayesfilter2023,
title = "Bayesian Filtering and Smoothing, Second Edition", 
author = "S. Särkkä and L. Svensson", 
publisher = Cambridge University Press,
year = 2023,
url = "http://users.aalto.fi/~ssarkka/pub/bfs_book_2023_online.pdf"
}
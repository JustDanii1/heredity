# CS50AI: Project 2 — Heredity

An AI program that assesses the probability distribution of genetic trait inheritance using **Bayesian Networks** and probabilistic inference.

This project was developed for Harvard University's **CS50’s Introduction to Artificial Intelligence with Python**.

## Overview

The application models genetic inheritance within a pedigree by evaluating:
* Population-wide gene probability distributions.
* Parent-to-child gene transmission, accounting for a $1\%$ mutation rate ($\mu = 0.01$).
* Probability of physical phenotype expression based on genotype ($0$, $1$, or $2$ gene copies).

The algorithm enumerates all possible joint assignments, calculates joint probabilities given observed evidence, and normalizes the results.

## Project Structure

* `heredity.py`: Main script containing joint probability calculations and Bayesian inference updates.
* `data/`: CSV files representing family trees (`family0.csv`, `family1.csv`, `family2.csv`).

## Usage

### Requirements
* Python 3.8+ (no external dependencies required).

### Execution

Run the script by passing a dataset path as a command-line argument:

```bash
python heredity.py data/family0.csv
```

## Sample Output

```text
Harry:
  Gene:
    2: 0.0092
    1: 0.4557
    0: 0.5351
  Trait:
    True: 0.2665
    False: 0.7335
James:
  Gene:
    2: 0.0022
    1: 0.0911
    0: 0.9067
  Trait:
    True: 0.0000
    False: 1.0000
Lily:
  Gene:
    2: 0.0143
    1: 0.9857
    0: 0.0000
  Trait:
    True: 1.0000
    False: 0.0000
```

## License

Created as part of [CS50 AI](https://cs50.harvard.edu/ai/).
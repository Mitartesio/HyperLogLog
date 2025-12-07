AppliedAlgorithmsAssignment2
This assignment is for applied algorithms assignment 2 by Andreas, Tobias and Frederik

# HyperLogLog: Probabilistic Cardinality Estimation in Java

This project implements the **HyperLogLog (HLL)** algorithm in Java to estimate the cardinality of large datasets using sublinear memory. The work focuses on hashing, the ρ-function, register size configuration, and empirical evaluation of estimation accuracy on datasets with up to **1,000,000 distinct elements**.

---

## Project Overview

HyperLogLog is a probabilistic data structure used to estimate the number of distinct elements in a multiset.  
This implementation includes:

- A custom **hashing pipeline** to ensure a uniform distribution of leading zeros  
- An implementation of the **ρ(x)** function for determining the position of the first set bit  
- Parameterized **register sizes (m)** for performance–accuracy trade-offs  
- A configurable **estimation and correction** pipeline following the HLL algorithm  

---

## Key Findings

Through experimentation and evaluation, the project demonstrated:

- **Correct distribution** of leading zeros across hashed values  
- **~0.54% variance** when estimating the cardinality of a dataset containing 1,000,000 distinct elements  
- Larger register sizes (**higher m**) significantly **reduce variance** and improve stability  
- Smaller register sizes are more **sensitive to outliers** and noise in the estimation  
- Probabilistic structures offer substantial **memory savings** while maintaining reliable accuracy  

---

## Experiments

Experiments included:

- Testing different register sizes  
- Measuring variance across repeated runs  
- Comparing estimates across differently generated datasets  
- Evaluating the effect of hash and ρ-function design on accuracy  

All experiments were automated and logged for reproducibility.

---

## Technologies Used

- **Java** (core implementation)  
- **JUnit** (evaluation & testing)  
- **Python** (optional supplementary analysis scripts)  

---

## What I Learned

This project strengthened my understanding of:

- Probabilistic data structures  
- Performance and space–accuracy trade-offs  
- Hash function behavior and uniformity  
- Scalable estimation techniques for large data systems  

---

## How to Run
Doing ``./gradlew clean build `` then making sure we generate the .jar files.

After which, simply run the Experiment.py file to generate the data from the gradle build. Utilize the various utility python files for post processing of the results csv.

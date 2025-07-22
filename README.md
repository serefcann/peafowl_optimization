# 🦚 Peacock Optimization Algorithm (POA)

This repository contains a simple implementation of a nature-inspired optimization algorithm — the **Peacock Optimization Algorithm (POA)** — to minimize the **Sphere Function**.

---

## 📌 Objective

The goal is to **find the minimum of the Sphere function**:

\[
f(x) = \sum_{i=1}^{n} x_i^2
\]

The global minimum of this function is at **x = [0, 0, ..., 0]** where **f(x) = 0**.

---

## 🛠️ Algorithm Description

This optimization algorithm mimics the behavior of peacocks:

- **Each peacock** represents a potential solution (a vector of real numbers).
- **The best peacock** is considered attractive, and others move toward it.
- **Movement** is a combination of attraction and randomness.
- **Mutation** simulates behavior changes and exploration.
- **Boundary constraints** ensure solutions stay within the valid range.

---

## 🔢 Parameters

| Parameter         | Description                                 |
|-------------------|---------------------------------------------|
| `n_tavuskusu`     | Number of peacocks in the population        |
| `n_iterasyon`     | Number of optimization iterations           |
| `boyut`           | Dimensionality of each solution (vector)   |
| `sinirlar`        | Bounds for each variable (e.g., -10 to 10)  |

---

## 🔄 Optimization Process

1. **Initialize** a population of peacocks with random positions within given bounds.
2. **Evaluate** each peacock's score using the objective function.
3. **Identify** the best-performing peacock.
4. For each iteration:
   - Each peacock:
     - Moves slightly toward the best peacock (attraction).
     - Adds randomness (exploration).
     - Has a 20% chance to mutate (normal noise).
     - Is clipped to remain within the bounds.
     - Is updated only if the new position improves its score.
     - If the new score is globally the best → update global best.
5. Every 10 iterations, print the best score so far.
6. At the end, print the **best solution and its score**.


---
  title: "Notes on Mathematics for Machine Learning"
---


# Chapter Two: Linear Algebra

## 2.1 Linear Equations
### 2.2.1 Definition

A set of **linear equations** $S$

$$S = \begin{cases}
a_{11}x_1 +  \dots + a_{1m}x_m \\
\dots \\
a_{1n}x_1 + \dots + a_{nm}x_{nm}
\end{cases}$$

has a solution if there is an $(x_1, x_2,\dots, x_n) \in \mathbb{R}^n$ such that
each equation in $S$ in satisfied.

### 2.2.2 Matrix Representation
A set of linear equations can be represented as matrix multiplication

$$
\begin{bmatrix}
a_{11} & a_{12} &  \dots & a_{1n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} &  \dots & a_{mn}
\end{bmatrix}
\begin{bmatrix}x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} =
\begin{bmatrix}b_1 \\ b_2 \\ \vdots \\ b_n \end{bmatrix}
$$

or $\mathbf{A}x=b$.

## 2.2 Matrices

### 2.2.1 Definition
A **matrix** is a two-dimensional tuple of values $[a_{ij}]$. An $m$ by $n$ real matrix is denoted $A \in \mathbb{R}^{m \times n}$

$$ A =
\begin{bmatrix}
a_{11} & a_{12} &  \dots & a_{1n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} &  \dots & a_{mn}
\end{bmatrix}
$$

### 2.2.2 Matrix Addition

Matrix addition is defined as

$$
A+B :=  \begin{bmatrix}
a_{11} + b_{11} & a_{12} + b_{12} &  \dots & a_{1n} + b_{1n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} + b_{m1} & a_{m2} + b_{m2} &  \dots & a_{mn} + b_{mn}
\end{bmatrix}
$$

### 2.2.2 Matrix Mutiplication

Matrix mutiplication between a matrix $A \in \mathbb{R}^{m \times n}$ and $B \in \mathbb{R}^{n \times m}$ is defined as

$$ (AB)_{ij} :=  \sum_k A_{ik}B_{kj} $$

Note that it is not commutative, i.e. $AB$ does not necessarily equal $BA$

### 2.2.3 Matrix Properties

1. **Associativity**:
 $$\forall (A \in \mathbb{R}^{m \times n}, B \in \mathbb{R}^{n \times p}, C \in \mathbb{R}^{p \times q}) : (AB)C = A(BC)$$

2. **Distributivity**:
$$\forall (A,B \in \mathbb{R}^{m \times n}), (C,D \in \mathbb{R}^{n \times p}) : (A+B)C = AC + BC, A(C+D) = AC+DC$$

3. **Identity**:
 $$\forall A \in \mathbb{R}^{n \times m} : I_m A = A, A I_n = A$$

### 2.2.4 Types of Matrices

1. **Inverse**: The inverse of $A \in \mathbb{R}^{m \times n}$ is a matrix $A^{-1}$ such that $AA^{-1}=I_n$. Not all matrices $A$ have inverses.

2. **Transpose**: The transpose of $A \in \mathbb{R}^{m \times n}$ is a matrix $A^T$ such that $A_{ij} = A^T_{ji} \ \forall i,j$

3. **Symmetric Matrix**: A matrix $A$ is symmetric if $A=A^T$

## 2.3 Solving Systems of Linear Equation

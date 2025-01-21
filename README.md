# IMU Calibration Using Affine Correction

## Introduction
This program calibrates a low-cost 3-axis accelerometer (IMU) by mapping raw sensor measurements to ground truth values using an affine correction function. The correction is computed through least squares minimization, producing a transformation matrix and bias vector.

---

## Problem Statement
Given:
1. **measurements.csv**: Raw three-axis accelerometer readings (\(\mathbf{r}\)).
2. **groundtruth.csv**: Accurate readings from a high-precision IMU (\(\mathbf{y}\)).

The goal is to find the affine correction function:
\[
\mathbf{y} = \mathbf{A} \mathbf{r} + \mathbf{b}
\]
where:
- \(\mathbf{A}\): \(3 \times 3\) transformation matrix.
- \(\mathbf{b}\): \(3 \times 1\) bias vector.

---

## Features
1. Reads raw and ground truth measurements from CSV files.
2. Computes \(\mathbf{A}\) and \(\mathbf{b}\) using least squares optimization.
3. Calculates the sum-of-squares error (SSE) to evaluate the correction function.
4. Outputs the computed correction parameters and error, with comments on the transformation.

---

## Requirements
- **Python 3.x**
- **Dependencies**:
  - `numpy`
  - `pandas`

Install required libraries:
```bash
pip install numpy pandas

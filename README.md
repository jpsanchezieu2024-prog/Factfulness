# Can the World Be Divided into Developed and Developing Countries?

## Project Overview

This project investigates whether the world can meaningfully be divided into only two groups — **developed** and **developing** countries — using a **data-driven clustering approach**.

The motivation comes from the ideas presented in the book *Factfulness* by Hans Rosling, which argues that the world should not be divided into just two groups but rather into **four or more levels of development**.

Using international development indicators and **unsupervised machine learning (K-Means clustering)**, we explore how many clusters naturally emerge from the data.

---

## Research Questions

1. **Can the world be meaningfully divided into only two clusters (developed vs developing)?**

   **Answer:** No.

2. **How many clusters are suggested by the data according to the Elbow Rule?**

   **Answer:** 5 clusters, explaining approximately **68% of the variance** in the data.

3. **How much of the data structure is explained by two clusters compared to the optimal number of clusters?**

   **Answer:**  
   - **2 clusters:** ~36% variance explained  
   - **5 clusters:** ~68% variance explained

4. **Does the evidence support the claim in *Factfulness* that the world cannot be divided into only two groups but into four or more?**

   **Answer:** Yes.  
   The analysis supports the idea that the world should not be split into only two groups. In fact, the data suggests **more than four clusters**, with **five clusters providing a better representation of global development differences.**

---

## Dataset

The dataset contains development indicators from the **United Nations** dataset, including variables such as:

- Life expectancy
- Income indicators
- Population statistics
- Health indicators
- Education measures

### Data Preparation

The following preprocessing steps were applied:

1. **Removed variables with more than 40% missing values**
2. **Dropped highly incomplete education variables**
3. **Imputed remaining missing values** using statistical imputation
4. **Prepared the dataset for clustering analysis**

---

## Methodology

### 1. Data Cleaning
- Missing values were analyzed
- Columns with excessive missing data were removed
- Remaining values were imputed

### 2. Feature Preparation
- Numerical variables were selected
- Data was standardized before clustering

### 3. K-Means Clustering

We applied **K-Means clustering** with different numbers of clusters (k).

### 4. Elbow Method

The **Elbow Rule** was used to determine the optimal number of clusters by analyzing how much variance is explained as k increases.

Results:

| Number of Clusters | Variance Explained |
|--------------------|--------------------|
| 2 | 36% |
| 3 | Higher but still limited |
| 4 | Significant improvement |
| **5 (Optimal)** | **68%** |

---

## Key Findings

### Two Clusters Are Too Simplistic

A model with only two clusters explains **only 36% of the variance**, meaning that a large portion of the differences between countries is lost.

This suggests that the traditional classification of:

- Developed countries
- Developing countries

is **too simplistic to capture real global differences.**

---

### Five Clusters Better Represent Global Development

Using the Elbow Rule, the data indicates that **five clusters** provide a much better structure, explaining **68% of the variance**.

This reveals multiple development levels rather than a simple binary classification.

---

## Connection to Factfulness

The findings align with the argument made in:

📚 **Factfulness – Hans Rosling**

Rosling argues that the world should not be divided into **two groups**, but rather **multiple levels of development**.

Our analysis confirms this claim:

- **Two groups:** Poor representation of reality
- **Four or more groups:** Much better representation
- **Five clusters:** Best solution in this dataset

Thus, the evidence **supports Rosling's argument**, and even suggests that **more than four groups may better capture global differences.**

---

## Conclusion

This project demonstrates that:

- The world **cannot meaningfully be divided into only two groups**.
- A **five-cluster model** better reflects global development differences.
- The analysis **supports the claims in *Factfulness*** that development exists on a **spectrum rather than a binary divide**.

---

## Repository Contents

| File | Description |
|-----|-------------|
| `UN.csv` | Dataset used for analysis |
| `ProjectPSDMA.ipynb` | Jupyter notebook with full analysis |
| `README.md` | Project documentation |

---

## How to Run the Project

```bash
git clone https://github.com/yourusername/world-development-clustering.git
cd world-development-clustering
pip install -r requirements.txt
jupyter notebook

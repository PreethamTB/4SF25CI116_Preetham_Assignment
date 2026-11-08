# Python Practice: File Handling, NumPy and Pandas

## Overview
This repository has three Jupyter notebooks with solved practice questions on file handling, NumPy and Pandas. Each question is written in a markdown cell, and the solution and its output are in the code cell below it.

## Files in this Repository
| File | Topic | Questions |
|------|-------|-----------|
| `FILE_HANDLING_1.ipynb` | Reading, writing and processing text files | 1 to 4 |
| `NUMPY_1.ipynb` | NumPy arrays, indexing, reshaping and structured arrays | 1 to 6 |
| `PANDAS_1.ipynb` | Pandas DataFrames, Series, grouping, merging and functions | 1 to 13 |

## 1. File Handling (`FILE_HANDLING_1.ipynb`)
| Q | Task | Approach |
|---|------|----------|
| 1 | Count the words in `document.txt` | Reads all lines with `readlines()` and adds up `len(line.split())` for each line |
| 2 | Find and replace a word in `data.txt` | Takes the word to find and the new word with `input()`, reads the file, uses `replace()`, and writes the result back |
| 3 | Print each line of `reverse.txt` reversed | Strips each line and prints it with slicing `[::-1]` |
| 4 | Count lines, words and characters in `stats.txt` | Returns three values from one function using `readlines()` and `split()` |

**Note:** `document.txt`, `data.txt`, `reverse.txt` and `stats.txt` must be in the same folder as the notebook before running it. Question 2 changes `data.txt` permanently.

## 2. NumPy (`NUMPY_1.ipynb`)
| Q | Task | Approach |
|---|------|----------|
| 1 | 5x5 array, replace the third column with 1 | Column slicing `a[:, 2] = 1` |
| 2 | 4x4 array from 1 to 16, set the diagonal to 0 | `np.fill_diagonal()` |
| 3 | 5x5 random integer array, extract the border elements | `np.random.randint()` and `np.concatenate()` of the first row, last column, last row and first column |
| 4 | 4x4 array from 1 to 16, row-wise and column-wise sum | `np.arange()`, `reshape()` and `np.sum()` with `axis=1` and `axis=0` |
| 5 | 3x3 array from 1 to 9, reshape to (1, 9) and (9, 1) | `reshape()` |
| 6 | Structured array with `name`, `age` and `weight`, sorted by age | A custom `dtype`, `np.sort(order="age")` and `np.append()` to add more records |

## 3. Pandas (`PANDAS_1.ipynb`)
| Q | Task | Approach |
|---|------|----------|
| 1 | DataFrame with 3 columns and 5 rows, add a column that is the product of the first two | Column multiplication with `iloc` |
| 2 | Row-wise and column-wise sum | `df.sum(axis=1)` and `df.sum(axis=0)` |
| 3 | Introduce NaN values and fill them with the column mean | `fillna()` with `mean()` |
| 4 | Drop rows that have any NaN value | `dropna()` |
| 5 | Group by `Category` and compute the sum and mean of `Value` | `groupby("Category")["Value"].agg(["sum", "mean"])` |
| 6 | DataFrame with `Product`, `Category` and `Sales` | Builds the DataFrame with random sales values using `random.randint()` |
| 7 | Merge two DataFrames on a common column | `pd.merge(df1, df2, on="X")` |
| 8 | MultiIndex DataFrame with indexing and slicing | `pd.MultiIndex.from_tuples()`, `loc` and `sort_index()` |
| 9 | MultiIndex of `Category` and `SubCategory`, sum of values | `groupby(level=...)` with `sum()` |
| 10 | Apply a function that doubles the values | `apply()` with a lambda function |
| 11 | Create a new column that is the sum of the existing columns | `apply()` with a lambda function and `axis=1` |
| 12 | Convert a Series of strings to uppercase | `str.upper()` |
| 13 | Extract the first three characters of each string | String slicing with `str[:3]` |

## Requirements
- Python 3
- NumPy
- Pandas
- Jupyter Notebook or JupyterLab

Install the libraries with:
```
pip install numpy pandas notebook
```

## How to Run
1. Clone or download this repository.
2. For `FILE_HANDLING_1.ipynb`, create the four text files listed above in the same folder.
3. Open each notebook in Jupyter and run the cells from top to bottom.

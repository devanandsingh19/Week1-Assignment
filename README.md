# 🐍 The Unlox Academy — Week 1 Master Assignment
### Python Fundamentals + NumPy Foundations

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-1.26-013243?logo=numpy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Questions](https://img.shields.io/badge/Questions-50%2F50-success)

> **50 interview-calibrated questions** covering Python fundamentals and NumPy foundations — part of the Data Science & Data Analytics track at [The Unlox Academy](https://unlox.in), an Outpro.India initiative.

---

## 📂 Repository Structure

```
week1-master-assignment/
│
├── Week1_MasterAssignment.ipynb   # Main notebook — all 50 solutions
└── README.md
```

---

## 📋 Assignment Overview

| Section | Topic | Questions |
|---------|-------|-----------|
| A | Theory — Interview Focus | Q1 – Q10 |
| B | Output Prediction | Q11 – Q15 |
| C1 | Coding — Warm-up | Q16 – Q20 |
| C2 | Coding — Conditionals & Logic | Q21 – Q25 |
| C3 | Coding — Nested Loop Patterns | Q26 – Q30 |
| C4 | Coding — Loop Logic | Q31 – Q36 |
| C5 | Coding — Lists, Tuples, Sets, Dicts | Q37 – Q42 |
| C6 | Coding — Strings | Q43 – Q45 |
| C7 | Coding — Functions | Q46 – Q47 |
| C8 | Coding — NumPy Foundations | Q48 – Q50 |

---

## 🔑 Key Concepts Covered

### Python Fundamentals
- `is` vs `==` — identity vs value equality
- Mutable vs immutable types (`list`, `tuple`, `str`, `frozenset`, etc.)
- Float precision and IEEE 754 representation
- Extended unpacking (`a, *b, c = [...]`)
- Short-circuit evaluation (`and`, `or`)
- List mutation traps — `x = x + [4]` vs `a += [4]`
- Loop variable scoping after `for`/`while`
- Integer arithmetic — `//`, `%`, `**` with negatives

### Data Structures
- Dictionary hashing and O(1) lookup
- Set operations — union, intersection, difference, symmetric difference
- Tuple as immutable record and dictionary key
- Word frequency analysis using `dict`
- Deduplication without `Counter` or `set` shortcuts

### Algorithms & Logic
- Armstrong numbers (1–9999)
- Fibonacci series (iterative, no recursion)
- Prime check optimised to √N
- Euclidean algorithm for HCF + LCM derivation
- Caesar cipher with wrap-around
- Single-pass string scanner (chars, words, vowels, digits, specials)
- Recursive `power(base, exp)` with negative exponent handling

### Real-World Problems
- 🇮🇳 Indian Income Tax calculator — New Regime FY 2024-25 (slab-wise)
- 🧾 PAN card format validator (no regex)
- ⚡ BESCOM electricity bill calculator (LT-2 Residential)
- 🛵 Swiggy order calculator with GST and delivery logic
- 🏏 Cricket strike rate classifier (T20 / ODI / Test)
- 📈 TCS stock price weekly analytics
- 🍕 Zomato Bengaluru sales analytics (NumPy, vectorised)

### NumPy
- `np.eye()`, `np.ones()`, `np.zeros()`, array slicing
- Vectorised operations — no explicit loops
- `np.argmax()`, `np.mean()`, `np.sum()`, `np.diag()`
- Day-on-day percentage change using array slicing
- Border pattern creation using slicing alone (Q50)

---

## 💡 Notable Questions

### Q11 — The list multiplication trap
```python
matrix1 = [[0] * 3 for _ in range(3)]   # 3 independent lists ✅
matrix2 = [[0] * 3] * 3                  # 3 references to the SAME list ⚠️
```

### Q12 — In-place vs rebinding
```python
a += [4]       # mutates in-place — all references see the change
x = x + [4]   # creates a new list — other references unaffected
```

### Q50 — NumPy border pattern (zero loops)
```python
border = np.ones((5, 5), dtype=int)
border[1:-1, 1:-1] = 0   # slice the interior to 0
```

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install numpy jupyter
```

### Run the notebook
```bash
git clone https://github.com/<your-username>/week1-master-assignment.git
cd week1-master-assignment
jupyter notebook Week1_MasterAssignment.ipynb
```

---

## 🧠 Key Takeaways

1. **`==` checks value; `is` checks memory identity** — never use `is` to compare values.
2. **`*` on a list of lists copies references, not objects** — always use a list comprehension to create independent rows.
3. **Float comparison with `==` is unreliable** — use `abs(a - b) < 1e-9`.
4. **`input()` always returns a string** — always cast explicitly.
5. **Non-empty containers are always truthy** — `bool([0])` is `True`.
6. **NumPy's power comes from avoiding loops** — if you're looping over a NumPy array, rethink the approach.

---

## 📊 Self-Assessment

| Score | Interpretation |
|-------|----------------|
| 45–50 | Strong foundation → move to Week 2 (Data Structures) |
| 30–45 | Revise weak topics → redo those questions |
| < 30  | Schedule a 1:1 with mentor, do not move to Week 2 yet |

---

## 🏫 About The Unlox Academy

The Unlox Academy is a structured Data Science & Data Analytics program by **Outpro.India**, designed to make learners interview-ready for product-based and service-based company roles. The curriculum is calibrated against real hiring rounds at companies like Razorpay, Flipkart, Swiggy, TCS, Infosys, and Wipro.

---

## 📄 License

This repository contains personal solutions to The Unlox Academy coursework. Intended for reference and learning — not for direct submission by others.

---

*"Code daily. Sleep when you must."* — Girish, Lead Mentor, The Unlox Academy

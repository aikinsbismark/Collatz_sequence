# Collatz Sequence

## Overview

The **Collatz Sequence**, also known as the **Collatz Conjecture** or the **3n+1** problem is one of the most famous unsolved problems in mathematics. Proposed by German mathematician **Lothar Collatz** in 1937. The sequence of numbers involved is sometimes referred to as the
**hailstone sequence**, or **hailstone numbers**.

## How It Works

The Collatz conjecture begins with **any positive integer** and repeatedly applies two simple arithmetic rules:

- If the current number is **even**, divide it by **2**.
- If the current number is **odd**, multiply it by **3** and add **1**.

The newly generated value becomes the next number in the sequence, and the process is repeated until the sequence reaches **1**.

---

## Mathematical Definition

For any positive integer \(n\):

$$
f(n)=
\begin{cases}
\dfrac{n}{2}, & \text{if } n \text{ is even} \\
3n+1, & \text{if } n \text{ is odd}
\end{cases}
$$

The function is applied repeatedly to each newly generated value until the sequence reaches **1**.

---

## Example

Suppose the starting number is:

```text
13
```

The sequence generated is:

```text
13 → 40 → 20 → 10 → 5 → 16 → 8 → 4 → 2 → 1
```

Step-by-step:

| Current Number | Operation | Next Number |
|---------------:|----------|------------:|
| 13 | 3 × 13 + 1 | 40 |
| 40 | 40 ÷ 2 | 20 |
| 20 | 20 ÷ 2 | 10 |
| 10 | 10 ÷ 2 | 5 |
| 5 | 3 × 5 + 1 | 16 |
| 16 | 16 ÷ 2 | 8 |
| 8 | 8 ÷ 2 | 4 |
| 4 | 4 ÷ 2 | 2 |
| 2 | 2 ÷ 2 | 1 |

Once the sequence reaches **1**, it enters the repeating cycle:

```text
1 → 4 → 2 → 1
```

Once the sequence reaches 1, it enters an infinite repeating cycle. Since no new values are produced beyond this point, most implementations terminate the algorithm when 1 is reached.

---

## Why Is the Collatz Conjecture Interesting?

The Collatz Conjecture is a perfect example of how simple rules can produce unexpectedly complex behavior. Every step follows a straightforward decision:

- Is the number even?
- If yes, divide by 2.
- Otherwise, multiply by 3 and add 1.

Despite this simplicity, mathematicians have been unable to determine why the process appears to work for every positive integer. Some numbers require only a few steps to reach **1**, while others produce sequences hundreds of terms long before eventually converging.

Modern computers have verified the conjecture for an enormous range of starting values, yet a complete mathematical proof remains undiscovered. This combination of simple logic and unsolved complexity continues to make the Collatz Conjecture one of mathematics' most famous open problems.

---

## About This Project

This project implements the Collatz Sequence in **Python**. It accepts a positive integer from the user and generates the corresponding sequence by repeatedly applying the Collatz rules until the value becomes **1**.

The project demonstrates fundamental programming concepts including:
- Flow control using `while` loops
- Conditional branching with `if` / `else` statements
- Exception handling with `try` / `except` blocks to handle non-integer inputs gracefully
- Integer division (`//`) to keep outputs clean

---

## 🚀 How to Run

1. Ensure you have [Python 3](https://python.org) installed.
2. Clone this repository or download the script.
3. Run the script in your terminal:
   ```bash
   python collatz_sequence.py
   ```

## License

This project is licensed under the MIT License.

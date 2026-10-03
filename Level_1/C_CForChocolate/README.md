# 1C: The slowest GCD

Part of [Level 1: Observe](../README.md). You need your **Enigma number E** (see the [main README](../../README.md#your-enigma-number-e)). The examples use E = 4671, from the username `math-cat7`.

**What to submit:** one pull request that adds your work to `Level_1/C_slowest_gcd/<your-github-username>/`. Any format is fine: a `solution.md`, a scanned PDF of handwritten pages, or photos of your pages. Keep each file under 2 MB.

---

## The story

You have a chocolate bar **a** cm by **b** cm. Each round, cut off as many of the biggest possible squares as fit. Repeat on the leftover piece until nothing is left. The side of the last square is the **GCD** (greatest common divisor) of a and b, and the number of rounds is the number of **steps**.

This is one of the oldest algorithms still in use. It's in Euclid's book *Elements*, written around 300 BC.

Example: an 8 × 5 bar. Round 1: cut one 5 × 5 square, leaving 5 × 3. Round 2: cut one 3 × 3 square, leaving 3 × 2. Round 3: cut one 2 × 2 square, leaving 2 × 1. Round 4: cut two 1 × 1 squares, and nothing is left. That's **4 steps**, and the GCD is 1.

Rules:

- Only use pairs (a, b) where **a ≥ b**, b is at least 1, and both are N or smaller.
- Every round counts as one step, including the last round, where the squares fit exactly and nothing is left over.

## Your limit

**N = 30 + (remainder of E ÷ 70).** Your N is between 30 and 99.

Example: 4671 ÷ 70 leaves remainder 51, so N = 81.

## What you do

1. **Guess:** which pair do you think takes the most steps? Write it down before calculating anything.
2. **Try examples:** find the steps for at least 5 pairs by hand and record them in a table.
3. **Find the slowest pair:** the pair (both N or smaller) with the most steps.
4. **Explain:** in 2–3 sentences, why is that pair so slow?

## Bonus (optional)

- Draw the square-cutting picture for your slowest pair.
- Without calculating, predict the slowest pair below 1000 and how many steps it takes.
- How many pairs up to your N tie for the most steps?

---

## What we expect to see

This is a guideline, not a form. Your work should cover these points, in any format. If you write a `solution.md`, these headings make a good outline:

```
# 1C: <your-github-username>

## My Enigma number

E = (show your working)

## 1C: The slowest GCD

My N (with working):

My guess:

My table:

Slowest pair and its steps:

Why it's slow:

## What surprised me

## Did I use AI? For what?
```

# 2C: The greedy cashier

Part of [Level 2: Break](../README.md). You need your **Enigma number E** (see the [main README](../../README.md#your-enigma-number-e)). The examples use E = 4671, from the username `math-cat7`.

**What to submit:** one pull request that adds your work to `Level_2/C_greedy_cashier/<your-github-username>/`. Any format is fine: a `solution.md`, a scanned PDF of handwritten pages, or photos of your pages. Keep each file under 2 MB.

---

## The story

The canteen gives change in tokens, and the cashier always follows one rule: **hand over the biggest token that fits, then repeat.** It's fast, and it sounds sensible.

**The claim:** "biggest-first always uses the fewest tokens." Break it, or show that for your tokens it really works.

## Your tokens

Take the **last 3 digits** of E (add zeros in front if needed). Call them d1, d2, d3, from left to right. Your tokens are worth 1, a, b and c, where:

- **a = 2 + d3**
- **b = a + 1 + d2**
- **c = b + 1 + d1**

Example: E = 4671 has last digits 6, 7, 1. So a = 3, b = 3 + 1 + 7 = 11, c = 11 + 1 + 6 = 18, and the tokens are **1, 3, 11, 18**.

## The two methods

```
BIGGEST-FIRST(amount):
    count = 0
    while amount > 0:
        t = the biggest token that is not bigger than amount
        amount = amount - t
        count = count + 1
    return count

BEST(amount):                     fill a table from 0 upwards
    best[0] = 0
    for x = 1 to amount:
        best[x] = 1 + the smallest of best[x - t],
                  over every token t that is not bigger than x
    return best[amount]
```

## A fact you may use

If biggest-first ever fails for 4 token values, it **already fails for some amount smaller than b + c** (your two biggest tokens added together). So you only need to check the amounts from 1 to b + c − 1.

## What you do

1. **Your tokens:** work them out from E.
2. **Guess:** does biggest-first always give the fewest tokens for your set?
3. **Fill the table:** for every amount from 1 to b + c − 1, write the biggest-first count and the best count side by side.
4. **Break it:** find the **smallest** amount where biggest-first uses more tokens than the best, and write down both ways of paying. If no amount in your table fails, explain why biggest-first always works for your tokens, using the fact above.
5. **Explain the failure:** why does grabbing the biggest token go wrong at that amount?
6. **Explain the table:** why does "1 + the smallest of best[x − t]" give the fewest tokens? Hint: think about the last token you hand over.

## Bonus (optional)

- Indian coins and notes are 1, 2, 5, 10, 20, 50, 100, 200, 500. Does biggest-first always work for them?
- Before 1971, British coins included values of 1, 3, 6, 12, 24 and 30 pennies. Find an amount where biggest-first fails.
- With just three tokens {1, a, b}, what's the **smallest amount** at which biggest-first can ever fail? Find the set.
- Design a token set where biggest-first fails as **badly** as possible at some amount.

---

## What we expect to see

This is a guideline, not a form. Your work should cover these points, in any format. If you write a `solution.md`, these headings make a good outline:

```
# 2C: <your-github-username>

## My Enigma number

E = (show your working)

## 2C: The greedy cashier

My tokens (with working):

My guess:

My table (amount, biggest-first, best):

Smallest failing amount and both payments (or: why it always works):

Why biggest-first fails here:

Why the table method works:

## What surprised me

## Did I use AI? For what?
```

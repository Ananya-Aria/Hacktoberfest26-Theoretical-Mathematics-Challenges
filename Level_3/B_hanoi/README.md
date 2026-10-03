# 3B: Tower of Hanoi with a broken peg

Part of [Level 3: Bend](../README.md). You need your **Enigma number E** (see the [main README](../../README.md#your-enigma-number-e)). The examples use E = 4671, from the username `math-cat7`.

**What to submit:** one pull request that adds your work to `Level_3/B_hanoi/<your-github-username>/`. Any format is fine: a `solution.md`, a scanned PDF of handwritten pages, or photos of your pages. Keep each file under 2 MB.

---

## The story

Three pegs stand in a row: **A** (left), **B** (middle) and **C** (right). A stack of disks sits on A, biggest at the bottom.

```
   |        |        |
  [1]       |        |
 [ 2 ]      |        |
[  3  ]     |        |
---A--------B--------C---
```

The rules:

- Move one disk at a time, always the top disk of a peg.
- Never put a bigger disk on top of a smaller one.

## Warm-up: the classic puzzle

In the classic puzzle you may move a disk between **any** two pegs. Here's the classic solution as a recursive method, one that uses a smaller copy of itself:

```
MOVE(n, from, to, spare):
    if n == 0: stop
    MOVE(n - 1, from, spare, to)          move the top n-1 disks out of the way
    move disk n from "from" to "to"
    MOVE(n - 1, spare, to, from)          put the n-1 disks back on top
```

## The bent rule

The middle peg is in the way. A disk may only move between **neighbouring** pegs: A↔B and B↔C. A disk can **never** jump straight between A and C.

## Your target

- If E is **even**, move the whole stack from A to **C**.
- If E is **odd**, move the whole stack from A to **B**.

Example: E = 4671 is odd, so the target is B.

## What you do

1. **Warm-up:** solve the classic puzzle (any moves allowed) for 1, 2 and 3 disks, moving from A to C. Count the moves and find the rule. Use the MOVE method to explain the rule.
2. **Guess:** with the broken peg, how many moves will 3 disks need to reach your target?
3. **Solve by hand:** under the bent rule, move 1 disk, then 2 disks, then 3 disks to your target. Write every move, for example "disk 1: A→B". Count the moves each time.
4. **Bend the method:** write a new recursive method, like MOVE, that follows the bent rule. How does moving n disks use moving n − 1 disks?
5. **Find the rule:** use your method to predict the moves for 4 disks and for 10 disks, without solving them by hand.
6. **Explain:** why is your method correct?

Tip: even if your target is B, you will need to understand moving disks all the way from A to C.

## Bonus (optional)

- Under the bent rule, list every arrangement of the disks your solution passes through when moving 3 disks from A to C. How many different arrangements are there? How many arrangements of 3 disks are possible in total?
- Compare the two targets. How is the number of moves for A to B related to the number for A to C?
- Why can no plan move the stack in fewer moves than yours? Hint: think about the biggest disk.

---

## What we expect to see

This is a guideline, not a form. Your work should cover these points, in any format. If you write a `solution.md`, these headings make a good outline:

```
# 3B: <your-github-username>

## My Enigma number

E = (show your working)

## 3B: Tower of Hanoi with a broken peg

Warm-up (classic): moves for 1, 2, 3 disks, and the rule:

My target (B or C) and why:

My guess for 3 disks:

My moves for 1, 2 and 3 disks (every move listed):

My bent recursive method:

My prediction for 4 disks and 10 disks:

Why my method is correct:

## What surprised me

## Did I use AI? For what?
```

# 1B: Find the fake coin

Part of [Level 1: Observe](../README.md). You need your **Enigma number E** (see the [main README](../../README.md#your-enigma-number-e)). The examples use E = 4671, from the username `math-cat7`.

**What to submit:** one pull request that adds your work to `Level_1/B_fake_coin/<your-github-username>/`. Any format is fine: a `solution.md`, a scanned PDF of handwritten pages, or photos of your pages. Keep each file under 2 MB.

---

## The story

Enigma's secretary has a big bag of coins (yep he truly does, find him later irl) ( jk jk ) that all look the same, but **one is fake and slightly heavier**. The only tool is a balance scale with two pans. Each use of the scale is one **weighing**, and it tells you one of three things: left pan heavier, right pan heavier, or balanced.

How few weighings guarantee finding the fake?

## How the scale works

- You can put any coins you like on each pan, and leave the rest off the scale.
- All the real coins weigh exactly the same. The fake is slightly heavier.

Your job is to come up with a plan: which coins to weigh each time, and what to do after each result. We care about the **worst case**: the most weighings your plan could ever need, however unlucky you are.

## Your coins

**n = 10 + (remainder of E ÷ 90).** Your n is between 10 and 99.

Example: 4671 ÷ 90 leaves remainder 81, so n = 91 coins.

## What you do

1. **Guess:** how many weighings do you think 27 coins need? Write it down first.
2. **Try halving:** put half the coins on each pan. How many weighings does 27 coins need in the worst case?
3. **Table:** find the fewest weighings for 2, 3, 4, … up to 27 coins.
4. **Find the rule:** where does the number of weighings go up by one?
5. **Your coins:** predict the fewest weighings for your n. Then write your full plan: how many coins go on each pan in every weighing, and what you do after each result. Check that the worst case matches your prediction.
6. **Explain:** why does splitting into three groups beat splitting into two? And why can **no plan at all** use fewer weighings than yours?

## Bonus (optional)

- **The famous version:** 12 coins, one fake, but you don't know whether it's **heavier or lighter**. Find the fake *and* say which it is, in 3 weighings.
- In that version, why can 3 weighings never handle 14 coins? Hint: count the possible answers.

---

## What we expect to see

This is a guideline, not a form. Your work should cover these points, in any format. If you write a `solution.md`, these headings make a good outline:

```
# 1B: <your-github-username>

## My Enigma number

E = (show your working)

## 1B: Find the fake coin

My n:

My guess for 27 coins:

Halving on 27 coins (worst case):

My table (2 to 27 coins):

The rule:

My prediction and my weighing plan:

Why three groups beat two:

Why no plan can do better:

## What surprised me

## Did I use AI? For what?
```

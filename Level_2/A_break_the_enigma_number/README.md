# 2A: Break the Enigma number

Part of [Level 2: Break](../README.md). You need your **Enigma number E** (see the [main README](../../README.md#your-enigma-number-e)). The examples use E = 4671, from the username `math-cat7`.

**What to submit:** one pull request that adds your work to `Level_2/A_break_the_enigma_number/<your-github-username>/`. Any format is fine: a `solution.md`, a scanned PDF of handwritten pages, or photos of your pages. Keep each file under 2 MB.

---

## The story

Everyone calculated an Enigma number from their username. **The claim:** "every username gets its own number." Prove that two different usernames can share a number. Then design a rule where that can never happen.

## Reminder: how E is calculated

a = 1, b = 2, … z = 26. Digits keep their own value, and `-` is 0. Multiply the 1st character by 1, the 2nd by 2, the 3rd by 4, and so on (doubling each time), then add everything up.

## What you do

1. **Guess:** do you think another username shares your Enigma number?
2. **Find a twin:** find a different username with exactly your E. It must follow GitHub's rules: only letters, digits and single hyphens, not starting or ending with a hyphen. It doesn't need to belong to a real person.
3. **Find a smarter twin:** find another username with your E, but this time **without** simply swapping a character for one with the same value (like `a` for `1`).
4. **Explain:** what are the two different reasons why two usernames can share a number?
5. **Fix it:** design a new rule where **no two usernames can ever share a number**.
6. **Prove your fix works.** Hint: if someone gives you only the number, can you work out the username?

## Bonus (optional)

- An early version of the rule multiplied by the position (1, 2, 3, …) instead of doubling. Find two usernames that collide under that rule too.
- How big does your new number get for your own username?
- Even with a perfect rule, two students can still get the same number of coins in task 1B. Why?

---

## What we expect to see

This is a guideline, not a form. Your work should cover these points, in any format. If you write a `solution.md`, these headings make a good outline:

```
# 2A: <your-github-username>

## My Enigma number

E = (show your working)

## 2A: Break the Enigma number

My guess:

Twin 1 (and its E, worked out):

Twin 2 (and its E, worked out):

The two reasons for collisions:

My new rule:

Why it can never collide:

## What surprised me

## Did I use AI? For what?
```

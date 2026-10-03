# 2D: Squeeze the weather report

Part of [Level 2: Break](../README.md). You need your **Enigma number E** (see the [main README](../../README.md#your-enigma-number-e)). The examples use E = 4671, from the username `math-cat7`.

**What to submit:** one pull request that adds your work to `Level_2/D_squeeze_the_weather/<your-github-username>/`. Any format is fine: a `solution.md`, a scanned PDF of handwritten pages, or photos of your pages. Keep each file under 2 MB.

---

## The story

In 1948, Claude Shannon wrote a paper that started a whole new field: **information theory**. He showed how to measure information in **bits**, and proved that there is a hard limit on how small a message can be squeezed. Every photo, call and video you send today relies on his ideas.

The university is trying to build a weather station on the campus roof, which sends one report per day: **Sunny (S)**, **Cloudy (C)**, **Rain (R)** or **Thunder (T)**. The reports travel over a slow radio link as 0s and 1s, and every bit costs.

## Your 16 days

Take the **last 3 digits** of E (add zeros in front if needed). Call them d1, d2, d3, from left to right.

- Cloudy days: **C = 1 + (remainder of d1 ÷ 4)**
- Rain days: **R = 1 + (remainder of d2 ÷ 3)**
- Thunder days: **T = 1 + (remainder of d3 ÷ 2)**
- Sunny days: **S = 16 − C − R − T**

Example: E = 4671 has last digits 6, 7, 1. So C = 1 + 2 = 3, R = 1 + 1 = 2, T = 1 + 1 = 2, and S = 16 − 7 = 9.

Now write your own 16-day report with exactly these numbers of days, in any order you like.

## How a code works

- Each kind of weather gets a **codeword** made of 0s and 1s, for example S = 00.
- The whole report is sent as one long string of bits, with no spaces or commas.
- The receiver must be able to split the string back into days, with no doubt at all.

A safe rule: **no codeword may be the beginning of another codeword.**

## Three claims to break

1. "There are 4 kinds of weather, so every day needs 2 bits. Your report needs 32 bits."
2. "With a clever enough code, you can squeeze your report as small as you like."
3. "A clever enough method can make **every** possible 16-day report shorter than 32 bits."

## A fact you may use: Shannon's limit

No code that gives each kind of weather its own codeword can send your report in fewer than **16 × H** bits, where H is Shannon's **entropy**: the average amount of information in one day's report. For your 16 days:

**16 × H = S × log₂(16 ÷ S) + C × log₂(16 ÷ C) + R × log₂(16 ÷ R) + T × log₂(16 ÷ T)**

You don't need a calculator for the logs. Use this table:

| Days              | 1 | 2 | 3     | 4 | 5     | 6     | 7     | 8 | 9     | 10    | 11    | 12    | 13    |
| ----------------- | - | - | ----- | - | ----- | ----- | ----- | - | ----- | ----- | ----- | ----- | ----- |
| log₂(16 ÷ days) | 4 | 3 | 2.415 | 2 | 1.678 | 1.415 | 1.193 | 1 | 0.830 | 0.678 | 0.541 | 0.415 | 0.300 |

## What you do

1. **Your days:** work out S, C, R and T, and write your 16-day report.
2. **Guess:** what's the fewest bits a clever code could use for your report?
3. **Break claim 1:** design a code that sends your report in **fewer than 32 bits**. Encode your report, then decode the bit string back to check it works. How many bits did you use?
4. **Find your best code:** try different codeword lengths. What's the fewest bits possible, with one codeword for each kind of weather?
5. **Break claim 2:** work out 16 × H using the table. Compare it with your best code. How close did you get?
6. **Break claim 3:** count how many different 16-day reports are possible (any of 4 kinds of weather each day), and how many different bit strings are shorter than 32 bits. What does that prove?
7. **Explain in your own words:** why should common weather get shorter codewords? And what does H measure?

## Bonus (optional)

- In task 1B, every weighing has 3 possible results. How many bits of information is one weighing worth? Use that to explain the rule you found in 1B.
- What is H if all four kinds of weather appear 4 times each? What if it's sunny all 16 days? Explain both in words.
- Make a code that breaks the safe rule (one codeword is the beginning of another). Find a bit string that can be read in two different ways.
- Look up David Huffman's method from 1952. Does it find your best code?

---

## What we expect to see

This is a guideline, not a form. Your work should cover these points, in any format. If you write a `solution.md`, these headings make a good outline:

```
# 2D: <your-github-username>

## My Enigma number

E = (show your working)

## 2D: Squeeze the weather report

My days (with working) and my 16-day report:

My guess:

My code, my report encoded, and decoded back:

My best code and its number of bits:

16 × H (with working), and how close my best code is:

Counting all reports vs shorter bit strings, and what it proves:

Why common weather gets shorter codewords, and what H measures:

## What surprised me

## Did I use AI? For what?
```

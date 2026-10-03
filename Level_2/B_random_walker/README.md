# 2B: The random walker

Part of [Level 2: Break](../README.md). You need your **Enigma number E** (see the [main README](../../README.md#your-enigma-number-e)). The examples use E = 4671, from the username `math-cat7`. This task also uses your map from [task 1A](../../Level_1/A_bridges/README.md).

**What to submit:** one pull request that adds your work to `Level_2/B_random_walker/<your-github-username>/`. Any format is fine: a `solution.md`, a scanned PDF of handwritten pages, or photos of your pages. Keep each file under 2 MB.

---

## The story

Remember your city from task 1A, with islands P, Q, R, S around the centre C and your own double bridges? A tourist with no plan arrives on island P. At every island they pick one of its bridges **completely at random** and cross it, then do it again, and again, for thousands of steps.

**The claim:** "the tourist visits every island equally often." Break it.

## The method

```
WALK(map, steps):
    island = P
    visits = 0 for every island
    repeat steps times:
        choose one bridge of this island at random
            (every bridge equally likely; a double bridge counts as two bridges)
        island = the island at the other end of that bridge
        visits[island] = visits[island] + 1
    return visits
```

An island's **share** is its visits divided by the total number of steps.

## Picking a random bridge by hand

Number the bridges at the current island 1, 2, 3, … and pick one at random:

- **Paper slips:** write the numbers on slips and draw one from a cup.
- **A die:** works for up to 6 bridges. Roll again if the number is too big.
- **A spreadsheet:** `=RANDBETWEEN(1, k)`, where k is the number of bridges.

## What you do

1. **Your map:** draw it again from 1A, and write how many bridges touch each island.
2. **Guess:** does the tourist visit every island equally? If not, which island wins, and by how much?
3. **Walk by hand:** 100 steps. Tally the visits to each island and work out the shares.
4. **Walk by computer:** at least 10,000 steps, using a spreadsheet or any programming language. Work out the shares again.
5. **Break the claim** with your numbers.
6. **Find the rule:** compare the shares with the bridge counts. What's the connection? Write it as a formula.
7. **Explain in words** why some islands get visited more than others.
8. **What randomness teaches you:** how close were your 100-step shares to your rule, and how close were your 10,000-step shares? What does that tell you about how many steps you need?

Include your code or spreadsheet in your folder.

## Bonus (optional)

- Start the tourist on C instead of P. Does your rule change?
- Use your rule to predict the shares for the real Königsberg (4 pieces of land, with 5, 3, 3 and 3 bridges).
- In your long run, count how often each bridge was crossed in each direction. What do you notice?
- How many steps does it take until every share is within 1% of your rule?

---

## What we expect to see

This is a guideline, not a form. Your work should cover these points, in any format. If you write a `solution.md`, these headings make a good outline:

```
# 2B: <your-github-username>

## My Enigma number

E = (show your working)

## 2B: The random walker

My map and the bridges touching each island:

My guess:

100 steps by hand (tally and shares):

10,000+ steps by computer (shares):

The claim is broken because:

My rule (formula):

Why it works, in words:

100 steps vs 10,000 steps, what I learned:

## What surprised me

## Did I use AI? For what?
```

# 3C: Fair matching

Part of [Level 3: Bend](../README.md). You need your **Enigma number E** (see the [main README](../../README.md#your-enigma-number-e)). The examples use E = 4671, from the username `math-cat7`.

**What to submit:** one pull request that adds your work to `Level_3/C_fair_matching/<your-github-username>/`. Any format is fine: a `solution.md`, a scanned PDF of handwritten pages, or photos of your pages. Keep each file under 2 MB.

---

## The story

Enigma wants to pair 4 new members (**A, B, C, D**) with 4 mentors (**1, 2, 3, 4**). Every member ranks the mentors, and every mentor ranks the members.

A pairing has a **problem** if a member and a mentor who are *not* paired together would *both* rather be with each other than with their current partners. A pairing with no problem like this is called **stable**.

## Your rankings

Take the **second-last digit** of E (the tens digit). If E is below 10, use 0. That's your set number. Example: E = 4671 gives set 7.

```
Set 0
Members (best first)    Mentors (best first)
A: 4 2 1 3              1: A D C B
B: 1 3 4 2              2: B D C A
C: 3 4 1 2              3: A D C B
D: 3 1 2 4              4: B A C D
```

```
Set 1
Members (best first)    Mentors (best first)
A: 1 2 3 4              1: B D A C
B: 3 2 4 1              2: D C A B
C: 1 3 4 2              3: C B D A
D: 4 2 3 1              4: C B A D
```

```
Set 2
Members (best first)    Mentors (best first)
A: 4 3 2 1              1: C B D A
B: 1 2 3 4              2: D A B C
C: 3 2 1 4              3: D A C B
D: 4 3 2 1              4: D A B C
```

```
Set 3
Members (best first)    Mentors (best first)
A: 4 3 2 1              1: A B D C
B: 2 4 3 1              2: C D B A
C: 2 1 3 4              3: B C D A
D: 1 4 3 2              4: C B A D
```

```
Set 4
Members (best first)    Mentors (best first)
A: 3 4 1 2              1: D A C B
B: 3 2 4 1              2: A C D B
C: 3 2 4 1              3: B A C D
D: 4 2 3 1              4: C A D B
```

```
Set 5
Members (best first)    Mentors (best first)
A: 4 3 2 1              1: B C D A
B: 3 1 2 4              2: A C D B
C: 2 1 4 3              3: C D B A
D: 2 4 3 1              4: C A B D
```

```
Set 6
Members (best first)    Mentors (best first)
A: 1 3 4 2              1: C D B A
B: 1 2 4 3              2: D B A C
C: 4 1 3 2              3: B A C D
D: 3 1 4 2              4: D C B A
```

```
Set 7
Members (best first)    Mentors (best first)
A: 4 3 1 2              1: C A D B
B: 1 4 2 3              2: A D B C
C: 2 1 4 3              3: B D C A
D: 1 3 2 4              4: C A D B
```

```
Set 8
Members (best first)    Mentors (best first)
A: 1 4 2 3              1: A C D B
B: 1 2 3 4              2: D B C A
C: 4 3 2 1              3: C A D B
D: 1 4 2 3              4: B A C D
```

```
Set 9
Members (best first)    Mentors (best first)
A: 3 4 2 1              1: A C B D
B: 3 1 4 2              2: D B C A
C: 4 1 2 3              3: C A B D
D: 3 4 2 1              4: D B C A
```

For example, in set 0, member A likes mentor 4 best, then 2, then 1, then 3.

## The method: propose and hold

```
PROPOSE-AND-HOLD(proposers, receivers):
    everyone starts unpaired
    while some proposer is unpaired:
        that proposer asks the best receiver they have not asked yet
        if the receiver is holding nobody:
            the receiver holds this proposer
        else if the receiver prefers this proposer to the one they are holding:
            the receiver holds this proposer, and the old one becomes unpaired
        else:
            the receiver says no
    return the pairs
```

"Hold" means "maybe": nothing is final until the very end.

## The bent rule

First, the **members** propose to the mentors. Then swap sides: the **mentors** propose to the members.

## What you do

1. **Your set:** copy your rankings into your solution.
2. **Guess:** before running anything, who do you think will end up with whom?
3. **Members propose:** run the method by hand. Keep a table of every proposal and what happened.
4. **Check stability:** for every member and mentor who are *not* paired together (12 combinations), show that they would not both rather be with each other.
5. **Bend it:** run the method again with the **mentors** proposing.
6. **Compare:** for each member and each mentor, which run gave them a better partner? What pattern do you see?
7. **Explain:** why does propose-and-hold always give a stable pairing? Hint: suppose member X prefers mentor 2 to their final partner. What happened when X asked mentor 2?

## Bonus (optional)

- Find **all** the stable pairings for your set by checking all 24 possible pairings. How many are there?
- When the members propose, can a mentor get a better partner by lying about their ranking?
- This method won the 2012 Nobel Prize in Economics. Look up how seat allocation in JoSAA counselling is related to it.

---

## What we expect to see

This is a guideline, not a form. Your work should cover these points, in any format. If you write a `solution.md`, these headings make a good outline:

```
# 3C: <your-github-username>

## My Enigma number

E = (show your working)

## 3C: Fair matching

My set number and rankings:

My guess:

Members propose (table of every proposal):

Stability check (all 12 combinations):

Mentors propose (table of every proposal):

Who did better in which run:

Why propose-and-hold is always stable:

## What surprised me

## Did I use AI? For what?
```

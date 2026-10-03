# 3A: The maze where you may break walls

Part of [Level 3: Bend](../README.md). You need your **Enigma number E** (see the [main README](../../README.md#your-enigma-number-e)). The examples use E = 4671, from the username `math-cat7`.

**What to submit:** one pull request that adds your work to `Level_3/A_maze/<your-github-username>/`. Any format is fine: a `solution.md`, a scanned PDF of handwritten pages, or photos of your pages. Keep each file under 2 MB.

---

## The story

You're in a maze of squares: `#` is a wall and `.` is open. You start at **S** (row 1, column 1) and must reach the exit **X** (row 7, column 7). Each step moves you up, down, left or right to a neighbouring square. The **length** of a path is its number of steps.

## Your maze

Take the **last digit** of E. That's your maze number. Example: E = 4671 gives maze 1.

**Maze 0**

```
    1 2 3 4 5 6 7
1   S . . # . . .
2   # . # . # . #
3   . . # # . . #
4   . # # . # # .
5   . # . . . # #
6   . . . # # . .
7   . . . # # . X
```

**Maze 1**

```
    1 2 3 4 5 6 7
1   S . # . . # #
2   # . # # . . .
3   . # # . . # #
4   . . # . # # #
5   . # . # . . .
6   . . . # . . .
7   . . . . . # X
```

**Maze 2**

```
    1 2 3 4 5 6 7
1   S . # . . # .
2   . # . . # # .
3   . . . # # . .
4   # . # # # . #
5   # # # . . . .
6   # . # . # . .
7   # # . . # # X
```

**Maze 3**

```
    1 2 3 4 5 6 7
1   S . . . . # #
2   # . . # . . .
3   . # . . # # #
4   . . . # . # .
5   . # # . # . .
6   . . . # . # #
7   . . . . # . X
```

**Maze 4**

```
    1 2 3 4 5 6 7
1   S # . . . . .
2   . # . # # . .
3   . . . # . # .
4   . . # . . . .
5   . # . . # # #
6   # . # . . . #
7   # . . . # # X
```

**Maze 5**

```
    1 2 3 4 5 6 7
1   S # # . . # .
2   # # . . . . .
3   . . . . # . .
4   . . # # . # .
5   # # . # # . .
6   . # # . # . #
7   # # # . # . X
```

**Maze 6**

```
    1 2 3 4 5 6 7
1   S . # . . . .
2   . . . . # . .
3   # # # . # # #
4   # . . # # . #
5   # # . . # . .
6   . . . . . # .
7   # # # # # . X
```

**Maze 7**

```
    1 2 3 4 5 6 7
1   S . . . . . .
2   # # # # # . .
3   . # . . . . .
4   # . . # # # #
5   . . . # . . #
6   # . . . # # .
7   . . . . . # X
```

**Maze 8**

```
    1 2 3 4 5 6 7
1   S # . . . . #
2   . . . # . # .
3   . . . # . # #
4   # . # . . . #
5   . . # . # . #
6   # . # . # # #
7   . # . . . # X
```

**Maze 9**

```
    1 2 3 4 5 6 7
1   S . . . . . #
2   # . # # # . .
3   . # # . . . .
4   # . . . . . #
5   . # # # # # #
6   # . # # # # .
7   . . . . . . X
```

## The method: flooding

The standard way to find the shortest path is to spread out from the start one step at a time, like water flooding the corridors. This is called **breadth-first search**.

```
FLOOD(maze):
    write 0 in the start square
    step = 0
    repeat:
        for every square that has the number step:
            write step + 1 in each open neighbour that has no number yet
        step = step + 1
    until no new numbers were written
    the number in the exit square is the length of the shortest path
```

On paper: write 0 in S, then 1 in every open square next to it, then 2 next to those, and so on.

## The bent rule

You may knock down up to **k walls**. Stepping onto a wall square knocks it down and uses up one of your breaks.

**A trick that helps:** draw your maze several times, as **floors**. Floor 0 means "I have broken 0 walls so far", floor 1 means "I have broken 1 wall", and so on. Stepping onto an open square keeps you on the same floor. Stepping onto a wall square takes you **up one floor**, onto that square. Now flood all the floors together, step by step.

## What you do

1. **Your maze:** copy it into your solution.
2. **Guess:** is there a path without breaking any walls? How long is the shortest path with 1 break? With 2 breaks?
3. **No breaks (k = 0):** flood your maze by hand. Is there a path?
4. **Bend it (k = 1 and k = 2):** use the floors to find the shortest path length for each. Draw both paths and mark the walls you broke.
5. **Explain:** why isn't "where am I" enough any more? Give an example square in your maze where knowing how many walls you've already broken changes what you can do next.
6. **Explain:** why does flooding always find the *shortest* path?

## Bonus (optional)

- What's the smallest k that gives the straight-as-possible path of 12 steps?
- How many squares do your three floors have in total when k = 2? Why is flooding them still quick?
- Can allowing one more break ever make the shortest path *longer*? Why or why not?

---

## What we expect to see

This is a guideline, not a form. Your work should cover these points, in any format. If you write a `solution.md`, these headings make a good outline:

```
# 3A: <your-github-username>

## My Enigma number

E = (show your working)

## 3A: The maze where you may break walls

My maze number and my maze:

My guess (k = 0, k = 1, k = 2):

k = 0, flooding by hand:

k = 1, shortest path length and the path (walls broken marked):

k = 2, shortest path length and the path (walls broken marked):

Why "where am I" isn't enough any more:

Why flooding finds the shortest path:

## What surprised me

## Did I use AI? For what?
```

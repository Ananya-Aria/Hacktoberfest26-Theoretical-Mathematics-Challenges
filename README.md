# Hacktoberfest 2026 : Theoretical & Mathematical Committee @ Enigma
Hello World :)

Guess -> Work it out -> Explain why

Welcome to the T&M committee's October challenge. There are **3 levels with 10 tasks in total**. Every task is about a 'real' idea from maths and computer science, and well most of them can be solved with pen paper and pseudocode, though if you like to code out verifications to those problems, or come up with solutions that require programming then, well ,you are more than welcome. You don't need to be a coder to take part. You need to be curious, and well gritty.

Every task asks you to **write down a guess or a presumption** **before you work anything out**. Being wrong is an interesting part, it will lead you to conclusions where we actually wanna go.

> **Note:** from 2026, the official Hacktoberfest no longer counts pull requests. This repository is Enigma's own October challenge, so your pull requests count here.
> We thought its nice to put this here, just so you people know, we are following the old model.

Well all the below 3 levels can , well, be attempted in any level you like, though we recommend that you go level by level and alphabettically.

| Level                       | Theme                                                                  | Tasks                                                                                                                |
| --------------------------- | ---------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| [Level 1](Level_1/README.md) | **Observe:** try small cases, spot the pattern, explain it       | 1A Bridges of your city<br />1B Find the fake coin <br /> 1C The slowest GCD                                        |
| [Level 2](Level_2/README.md) | **Break:** find the one example that proves a claim wrong        | 2A Break the Enigma number<br />2B The random walker <br />2C The greedy cashier <br />2D Squeeze the weather report |
| [Level 3](Level_3/README.md) | **Bend:** take a known method, change one rule, see what happens | 3A The maze where you may break walls<br /> 3B Tower of Hanoi with a broken peg <br /> 3C Fair matching             |

---

## Your Enigma number (E)

Every task uses your **Enigma number**, so your problems are different from your friends . You calculate it from your GitHub username:

1. Write your GitHub username in small letters.
2. Give each character a value: a = 1, b = 2, … z = 26. Digits keep their own value. A hyphen `-` is 0.
3. Multiply the 1st character by 1, the 2nd by 2, the 3rd by 4, the 4th by 8, and so on, doubling each time.
4. Add everything up. That total is **E**.

Don't think the larger the number the more cases you will have to try out or the worse it will be.. my enigma number is 60311 as well, so dw I got you.

**Example:** the username `math-cat7`

| Position | Character | Value | Multiplier  | Result         |
| -------- | --------- | ----- | ----------- | -------------- |
| 1        | m         | 13    | 1           | 13             |
| 2        | a         | 1     | 2           | 2              |
| 3        | t         | 20    | 4           | 80             |
| 4        | h         | 8     | 8           | 64             |
| 5        | -         | 0     | 16          | 0              |
| 6        | c         | 3     | 32          | 96             |
| 7        | a         | 1     | 64          | 64             |
| 8        | t         | 20    | 128         | 2560           |
| 9        | 7         | 7     | 256         | 1792           |
|          |           |       | **E** | **4671** |

The letters are taken at the alphabettical order, like a is 1 and b is 2 and so on

Don't forget to put your working for E at the top of every submission.

---

## Ground rules

- **Deadline:** 31 October 2026, 23:59 IST.
- **Your folder:** every task has its own folder, and you make your own folder inside it: `Level_N/<task-folder>/<your-github-username>/`, for example :`Level_1/A_bridges/math-cat7/`. Only add or change files inside your own folder.
- **One pull request per task.** If something needs fixing, push more commits to the same pull request. Don't open a new one.
- **At most two open pull requests at a time.** When one is merged, you can open another.
- **Pseudocode is welcome.** Any programming language is fine too. Code is optional, except where a task asks for a computer run.
- **Guess first.** Every task starts with a guess. Write it before you calculate anything.
- **Any format, small files.** A `solution.md`, a scanned PDF of handwritten pages, or photos are all fine. Keep each file under 2 MB. For handwritten work, a phone scanner app (like the scanner in Google Drive, or Adobe Scan) makes small, readable PDFs. Needless to say, please see to it that your work is legible.

---

## Use of tools

Please don't treat this as a list of tasks to finish for pull requests. It's a chance to see what the Theoretical and Mathematical Committee is about, and maybe to find out if you enjoy this.

- **Try it yourself first**, and give it real time.
- **Then talk to people**: ask in the Enigma group or discuss with friends. Discussing is encouraged; write your own solution afterwards.
- **Use AI tools only if you're genuinely stuck**, and only for a hint. They often get the details of these tasks wrong.

You do **not** need to know how to code. Pseudocode, reasoning and plain English are just as welcome.

Read the full rules in [USE_OF_TOOLS.md](USE_OF_TOOLS.md) before you start, and follow them strictly.

---

## How to take part

1. Read [CONTRIBUTING.md](CONTRIBUTING.md) for the step-by-step git guide. (We know the git workshop went a little too deep, this is just the essentials, I promise.)
2. Calculate your Enigma number.
3. Pick a task and read its README. Each level has its own task folders (A, B, C, and D in Level 2).
4. Put your work in `Level_N/<task-folder>/<your-github-username>/`: a `solution.md`, a scanned PDF of handwritten pages, or photos. The end of each task's README lists what we expect to see.
5. Open one pull request for that task.

Questions? Open an issue in this repository or ask us in the Enigma discord chat or the student or devs community whatsapp group.

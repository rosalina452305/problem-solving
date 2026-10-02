# Repository Guidelines

This document defines the organization, naming, documentation, classification, and commit conventions used by the `problem-solving` repository.

The repository is intended to preserve useful problem-solving knowledge while still allowing less educational submissions to be archived when desired.

---

# 1. Repository Structure

```text
problem-solving/
├── README.md
├── GUIDELINES.md
├── LICENSE
│
├── Codeforces/
├── AtCoder/
├── Luogu/
├── LeetCode/
├── CodeChef/
│
└── MISC/
```

Only judges that are actually in use should receive top-level directories.

Additional judges may be added when needed.

Do not create directories in advance merely for completeness.

---

# 2. Educational Classification

Difficulty and educational value are different concepts.

A difficult problem may contain little reusable knowledge, while a simple problem may demonstrate an important pattern or implementation technique.

The location and documentation of a problem should therefore depend on what is worth preserving from it.

## 2.1 Normal Educational Value

Problems containing clearly useful knowledge belong to their corresponding judge.

Useful material may include:

- algorithms;
- data structures;
- mathematical observations;
- transformations;
- implementation techniques;
- reusable patterns;
- proofs;
- edge cases;
- common pitfalls;
- alternative approaches.

```text
<Judge>/<Problem-ID>.<ext>
```

---

## 2.2 Low Educational Value

Problems with only limited educational value may still remain under their corresponding judge.

Examples include:

- basic implementation exercises;
- straightforward simulations;
- routine applications of familiar algorithms;
- simple practice problems;
- problems whose main value is reinforcing an existing technique.

For example:

```text
Codeforces/CF-XXXXXA.cpp
AtCoder/ABC-XXXXXA.cpp
```

Low educational value alone is **not** sufficient reason to move a problem into `MISC/`.

If there is still something worth practicing, reviewing, or remembering, the problem may remain under its original judge.

---

## 2.3 Minimal or No Educational Value

Some solved problems may be worth preserving even though they provide almost no reusable problem-solving knowledge.

These belong in:

```text
MISC/
```

Typical examples include:

- joke problems;
- April Fools problems;
- fixed-output problems;
- one-off visual or logic puzzles;
- solutions based almost entirely on information unique to that problem;
- submissions preserved primarily for archival purposes.

The distinction is:

```text
Worth studying, reviewing, or practicing
        │
        └── <Judge>/

Worth preserving mainly as an archive
        │
        └── MISC/
```

`MISC/` means **archival**, not incorrect or poor quality.

---

# 3. Placeholder Convention

Documentation uses placeholders instead of real problem numbers.

```text
X        = one numeric digit

XXXXX    = five-digit sequential identifier
XXXXXX   = six-digit sequential identifier

XXXXXXX  = arbitrary slug or opaque problem code

A        = problem/task index

<...>    = descriptive placeholder
```

`XXXXXXX` does **not** mean that a slug must contain exactly seven characters.

It simply represents an arbitrary identifier whose internal structure should not be interpreted.

Actual source files always use their real problem identifiers.

---

# 4. Naming Convention

Problem identifiers should preserve the semantics of their original online judges.

Zero-padding is used only for genuine sequential numeric identifiers.

Digits inside opaque problem codes or slugs are preserved unchanged.

---

# 5. Codeforces

Format:

```text
CF-XXXXXA
```

Structure:

```text
CF-
│
├── XXXXX    contest number
└── A        problem index
```

The contest number is represented using five digits.

Possible forms include:

```text
CF-XXXXXA
CF-XXXXXB
CF-XXXXXC
CF-XXXXXF
```

File:

```text
Codeforces/CF-XXXXXA.cpp
```

Study directory:

```text
Codeforces/
└── CF-XXXXXF/
    ├── solution.cpp
    └── README.md
```

---

# 6. AtCoder

The contest series is preserved as part of the identifier.

Formats:

```text
ABC-XXXXXA
ARC-XXXXXA
AGC-XXXXXA
AHC-XXXXXA
```

Structure:

```text
ABC-
 │
 ├── XXXXX    contest number
 └── A        task identifier
```

Files:

```text
AtCoder/ABC-XXXXXA.cpp
AtCoder/ARC-XXXXXA.cpp
AtCoder/AGC-XXXXXA.cpp
AtCoder/AHC-XXXXXA.cpp
```

Different AtCoder contest series remain distinguishable even when their numeric identifiers overlap.

---

# 7. Luogu

Format:

```text
LG-PXXXXXX
```

Structure:

```text
LG-P
   │
   └── XXXXXX    numeric problem identifier
```

The numeric portion uses six digits.

File:

```text
Luogu/LG-PXXXXXX.cpp
```

Study directory:

```text
Luogu/
└── LG-PXXXXXX/
    ├── solution.cpp
    └── README.md
```

---

# 8. LeetCode

Format:

```text
LC-XXXXX
```

Structure:

```text
LC-
 │
 └── XXXXX    numeric problem identifier
```

The numeric portion uses five digits.

File:

```text
LeetCode/LC-XXXXX.cpp
```

Study directory:

```text
LeetCode/
└── LC-XXXXX/
    ├── solution.cpp
    └── README.md
```

---

# 9. CodeChef

CodeChef problem codes are treated as opaque identifiers.

Format:

```text
XXXXXXX
```

File:

```text
CodeChef/XXXXXXX.cpp
```

The official problem code should be preserved.

Digits appearing inside the problem code must not be independently zero-padded or rearranged.

The placeholder `XXXXXXX` represents an arbitrary problem code and does not impose a fixed length.

Study directory:

```text
CodeChef/
└── XXXXXXX/
    ├── solution.cpp
    └── README.md
```

---

# 10. MISC

`MISC/` is an archival area for solutions with minimal or no educational value.

Whenever possible, the original normalized problem identifier should still be preserved.

Examples:

```text
MISC/CF-XXXXXF.cpp
MISC/ABC-XXXXXA.cpp
MISC/LG-PXXXXXX.cpp
MISC/LC-XXXXX.cpp
MISC/XXXXXXX.cpp
```

Moving a problem into `MISC/` does not change its identifier.

This makes the original source easy to recognize and search for.

---

# 11. Normal Solution Files

Most archived problems should remain single source files.

General form:

```text
<Judge>/<Problem-ID>.<ext>
```

Examples:

```text
Codeforces/CF-XXXXXA.cpp
AtCoder/ABC-XXXXXA.cpp
Luogu/LG-PXXXXXX.cpp
LeetCode/LC-XXXXX.cpp
CodeChef/XXXXXXX.cpp
```

A single file means:

> The source code and a short header are sufficient to preserve what is worth keeping.

---

# 12. Source Header

Every stored solution should contain a short identification header when an original problem page is available.

Minimum form:

```cpp
// <Problem-ID> - <Problem Title>
// <Problem URL>
```

For example:

```cpp
// CF-XXXXXA - <Problem Title>
// <Problem URL>
```

If the problem contains a concise lesson worth remembering, add an `Idea` line:

```cpp
// CF-XXXXXA - <Problem Title>
// <Problem URL>
// Idea: <one-sentence takeaway>
```

The `Idea` line is optional.

It should answer:

> What is the one thing worth remembering from this problem?

The source header should remain short.

Do not turn it into a full editorial.

Avoid unnecessary metadata such as:

```text
Submission ID
Runtime
Memory usage
Solved status
Programming language
Date
```

unless that information is specifically relevant.

---

# 13. Documentation Levels

The amount of documentation should correspond to the amount of knowledge worth preserving.

## Level 0 — Archive

```text
MISC/<Problem-ID>.<ext>
```

Examples:

```text
MISC/CF-XXXXXF.cpp
MISC/XXXXXXX.cpp
```

Use this when the solution is worth preserving but provides almost no educational value.

The problem URL should still be included when available.

---

## Level 1 — Simple Solution

```text
<Judge>/<Problem-ID>.<ext>
```

Example:

```text
Codeforces/CF-XXXXXA.cpp
```

Header:

```cpp
// CF-XXXXXA - <Problem Title>
// <Problem URL>
```

Use this for straightforward or low-value problems where the implementation itself is sufficient.

---

## Level 2 — Annotated Solution

```text
<Judge>/<Problem-ID>.<ext>
```

Header:

```cpp
// CF-XXXXXA - <Problem Title>
// <Problem URL>
// Idea: <one-sentence takeaway>
```

Use this when a short observation captures the main educational value.

---

## Level 3 — Study

```text
<Judge>/
└── <Problem-ID>/
    ├── solution.cpp
    └── README.md
```

Example:

```text
Codeforces/
└── CF-XXXXXF/
    ├── solution.cpp
    └── README.md
```

Use this when source code alone cannot adequately preserve the reasoning worth learning.

---

## Level 4 — Deep Study

```text
<Judge>/
└── <Problem-ID>/
    ├── solution.cpp
    ├── solution-alt.cpp
    ├── brute.cpp
    ├── generator.cpp
    ├── README.md
    └── tests/
        ├── XX.in
        ├── XX.out
        └── ...
```

Possible reasons for using this structure include:

- multiple meaningful solutions;
- nontrivial correctness proofs;
- optimization from brute force;
- stress testing;
- counterexample construction;
- implementation subtleties;
- reusable techniques worth studying in depth.

Only create files that provide actual value.

---

# 14. Study Directory

A problem may naturally evolve from a single source file:

```text
CF-XXXXXF.cpp
```

into a directory:

```text
CF-XXXXXF/
```

The canonical problem identifier does not change.

Minimum:

```text
CF-XXXXXF/
├── solution.cpp
└── README.md
```

Optional:

```text
solution-alt.cpp
brute.cpp
generator.cpp
tests/
```

File meanings:

| File | Purpose |
| --- | --- |
| `solution.cpp` | Primary solution |
| `solution-alt.cpp` | Meaningfully different alternative solution |
| `brute.cpp` | Brute-force or reference implementation |
| `generator.cpp` | Test-case generator |
| `README.md` | Detailed analysis |
| `tests/` | Useful tests, counterexamples, or generated cases |

Do not create empty files merely to satisfy a template.

---

# 15. Problem README

A problem-level `README.md` records **what is worth learning from the problem**.

It should not reproduce the original problem statement.

Recommended structure:

```markdown
# <Problem-ID> — <Problem Title>

<Problem URL>

## Key Idea

Explain the central insight.

## Observations

Explain the observations leading to the solution.

## Solution

Explain the algorithm.

## Correctness

Explain why the algorithm works.

## Complexity

- Time: O(...)
- Space: O(...)

## Notes

Record pitfalls, implementation details, alternative ideas, or further observations.
```

Not every section is mandatory.

For a smaller study:

```markdown
# <Problem-ID> — <Problem Title>

<Problem URL>

## Key Idea

...

## Complexity

- Time: O(...)
- Space: O(...)
```

Additional sections may be introduced when useful:

```text
Derivation
Proof
Pitfalls
Counterexamples
Alternative Solutions
Brute Force
Optimization
Implementation Notes
Further Thoughts
```

The goal is to document the lesson, not duplicate the statement.

---

# 16. File Extensions

Use conventional source-file extensions.

```text
C++       .cpp
Python    .py
Rust      .rs
Java      .java
Markdown  .md
Input     .in
Output    .out
Shell     .sh
```

Examples:

```text
Codeforces/CF-XXXXXA.cpp
AtCoder/ABC-XXXXXA.py
Luogu/LG-PXXXXXX.cpp
LeetCode/LC-XXXXX.cpp
CodeChef/XXXXXXX.cpp
```

Do not introduce language-specific directory trees unless there is a practical need.

---

# 17. Commit Messages

Commit messages should identify the operation and the canonical problem identifier.

Format:

```text
<type>: <Problem-ID> [description]
```

Recommended types:

```text
add
study
fix
docs
refactor
chore
```

Examples:

```text
add: CF-XXXXXA
add: ABC-XXXXXA
add: LG-PXXXXXX
add: LC-XXXXX
add: XXXXXXX
```

For deeper work:

```text
study: CF-XXXXXF
docs: CF-XXXXXF
fix: LC-XXXXX
refactor: LG-PXXXXXX
```

For MISC:

```text
add: CF-XXXXXF to MISC
add: XXXXXXX to MISC
```

For specific changes:

```text
add: CF-XXXXXF alternative solution
fix: CF-XXXXXF overflow
docs: CF-XXXXXF correctness proof
```

Keep commit messages concise.

The problem identifier should remain the primary reference.

---

# 18. Decision Guide

When deciding where a solution belongs:

```text
Does the problem contain something worth
studying, reviewing, or practicing?
│
├── No
│   │
│   └── MISC/<Problem-ID>.<ext>
│
└── Yes
    │
    ├── Is the source code itself sufficient?
    │   │
    │   ├── Yes
    │   │   │
    │   │   └── <Judge>/<Problem-ID>.<ext>
    │   │
    │   └── Mostly
    │       │
    │       └── Add a one-line Idea comment.
    │
    └── Does understanding it require
        substantial explanation?
        │
        └── Yes
            │
            └── <Judge>/<Problem-ID>/
                ├── solution.<ext>
                └── README.md
```

Low educational value does **not** automatically imply `MISC`.

The important distinction is:

```text
Still useful to revisit
    → Judge

Only useful to preserve
    → MISC
```

---

# 19. Adding New Judges

The currently defined judges are:

```text
Codeforces
AtCoder
Luogu
LeetCode
CodeChef
```

Do not define naming rules for unused judges in advance.

When another judge becomes relevant:

1. determine its canonical problem identifier;
2. determine whether the identifier contains a genuine sequential number or an opaque slug;
3. choose a reasonable zero-padding width only when useful;
4. document the convention in this file;
5. create the judge directory.

This keeps the repository conventions based on actual use rather than hypothetical future requirements.

---

# 20. Core Principles

## Educational value over completeness

The main judge directories are a curated problem-solving collection rather than a complete accepted-submission archive.

## Low value is still value

Simple and routine problems may remain under their original judges when they are still useful for practice or review.

## MISC is archival

`MISC/` contains solutions worth preserving but with little or no meaningful educational value.

## Preserve canonical identifiers

Problem identifiers should remain consistent across filenames, directories, source headers, documentation, and commit messages.

## Pad sequences, not arbitrary digits

Zero-padding exists for stable and readable sorting.

Opaque problem codes and slugs should not be modified.

## Keep simple problems simple

A single source file is preferred when it is sufficient.

## Explain the lesson, not the statement

Detailed documentation should preserve insights, reasoning, proofs, pitfalls, and reusable knowledge rather than copying the original problem statement.

## Let problems grow naturally

A problem may begin as a simple source file and later become a study directory when deeper analysis becomes worthwhile.

## Add infrastructure only when needed

New judge directories, naming conventions, documentation sections, and auxiliary files should be introduced when they solve an actual organizational need.
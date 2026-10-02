# problem-solving

My solutions, practice code, and study notes for competitive programming and online judges.

This repository is organized primarily by **online judge** and **educational value**.

It is not intended to be a complete collection of every accepted submission. Problems with educational or review value are kept under their corresponding judges, while solutions preserved mainly for archival purposes are placed under `MISC/`.

## Structure

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

Only judges currently in use are included. Additional judge directories may be added when needed.

## Organization

Problems with at least some value for learning, reviewing, or practicing are stored under their corresponding judge.

```text
Codeforces/CF-XXXXXA.cpp
AtCoder/ABC-XXXXXA.cpp
Luogu/LG-PXXXXXX.cpp
LeetCode/LC-XXXXX.cpp
CodeChef/XXXXXXX.cpp
```

Low educational value does **not** automatically mean that a problem belongs in `MISC/`.

A simple implementation problem, familiar pattern, or routine exercise may still be useful for practice or review and therefore remain under its original judge.

`MISC/` is reserved for solutions that are worth preserving but provide little or no meaningful problem-solving value.

Examples include:

- joke or April Fools problems;
- fixed-output problems;
- one-off puzzles;
- solutions based on problem-specific information with little reusable knowledge;
- submissions preserved mainly for archival purposes.

## Documentation

A normal problem is stored as a single source file:

```text
Codeforces/
└── CF-XXXXXA.cpp
```

When useful, the source header contains a short takeaway:

```cpp
// CF-XXXXXA - <Problem Title>
// <Problem URL>
// Idea: <one-sentence takeaway>
```

Problems requiring deeper explanation are stored as directories:

```text
Codeforces/
└── CF-XXXXXF/
    ├── solution.cpp
    └── README.md
```

Additional research files such as `brute.cpp`, `generator.cpp`, alternative solutions, or tests are added only when they provide actual value.

## Naming

The main naming formats are:

```text
Codeforces   CF-XXXXXA
AtCoder      ABC-XXXXXA
             ARC-XXXXXA
             AGC-XXXXXA
             AHC-XXXXXA
Luogu        LG-PXXXXXX
LeetCode     LC-XXXXX
CodeChef     XXXXXXX
```

`X` represents a numeric digit when used in a numeric identifier.

`XXXXXXX` represents an arbitrary slug or opaque problem code and does **not** imply a fixed length.

For the complete repository conventions, see [GUIDELINES.md](GUIDELINES.md).

## License

See [LICENSE](LICENSE).
# "99 Bottles of Beer" kata in Python

[![CI](https://github.com/Coding-Cuddles/99-bottles-of-beer-python-kata/actions/workflows/main.yml/badge.svg)](https://github.com/Coding-Cuddles/99-bottles-of-beer-python-kata/actions/workflows/main.yml)
[![Python 3.11+](https://img.shields.io/badge/python-3.11%2B-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## Overview

This kata complements [Clean Code: Advanced TDD, Ep. 24](https://cleancoders.com/episode/clean-code-episode-24-p1).

This repository contains an exercise to construct the entire
[99 Bottles of Beer](http://en.wikipedia.org/wiki/99_Bottles_of_Beer) song
using TDD.

### Exercise

Complete the `Bottles.song()` method that returns the lyrics for the song
"99 Bottles of Beer" as an **array of strings** where each string represents
a line of the song:

> 99 bottles of beer on the wall, 99 bottles of beer.</br>
> Take one down and pass it around, 98 bottles of beer on the wall.
> 
> 98 bottles of beer on the wall, 98 bottles of beer.</br>
> Take one down and pass it around, 97 bottles of beer on the wall.
> 
> ...
> 
> 3 bottles of beer on the wall, 3 bottles of beer.</br>
> Take one down and pass it around, 2 bottles of beer on the wall.
> 
> 2 bottles of beer on the wall, 2 bottles of beer.</br>
> Take one down and pass it around, 1 bottle of beer on the wall.
> 
> 1 bottle of beer on the wall, 1 bottle of beer.</br>
> Take one down and pass it around, no more bottles of beer on the wall.
> 
> No more bottles of beer on the wall, no more bottles of beer.</br>
> Go to the store and buy some more, 99 bottles of beer on the wall.

## Prerequisites

Required:

- [Git](https://git-scm.com/downloads)
- [uv](https://docs.astral.sh/uv/getting-started/installation/)

Optional:

- [GNU Make](https://www.gnu.org/software/make/), for shorter commands. Every required task also
  has a direct `uv` command.

You do not need to install Python or pytest separately. `uv` installs a compatible Python version
and the locked project dependencies when needed.

## Set up the kata

1. Clone the repository:

   ```console
   git clone https://github.com/Coding-Cuddles/99-bottles-of-beer-python-kata.git
   ```

2. Enter the repository directory:

   ```console
   cd 99-bottles-of-beer-python-kata
   ```

3. Run the existing test. Use Make when it is installed:

   ```console
   make test
   ```

   Otherwise, run pytest through `uv` directly:

   ```console
   uv run pytest test_*.py
   ```

   The first run may install Python and the project dependencies. Setup is complete when pytest
   reports `1 passed`.

   If the command fails with `uv: command not found`, install
   [uv](https://docs.astral.sh/uv/getting-started/installation/) and repeat this step.

## Work on the kata

1. Add the next behavior to `test_bottles.py`, then implement it in `bottles.py`.

2. Run the tests after each change. Use Make when it is installed:

   ```console
   make test
   ```

   Otherwise, run pytest through `uv` directly:

   ```console
   uv run pytest test_*.py
   ```

   Continue when the test run passes.

## Make command reference

Make is optional. Run `make` or `make help` to list these commands in the terminal.

| Command             | Result                                  |
| ------------------- | --------------------------------------- |
| `make all`          | Run the test suite                      |
| `make help`         | List public Make targets                |
| `make test`         | Run the test suite                      |
| `make format`       | Format tracked Python files             |
| `make format-check` | Check formatting without changing files |
| `make clean`        | Remove generated caches                 |

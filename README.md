# Advent Of Code 2022: Tutorial Solutions in Rust
Copyright (c) 2022 Benjamin and Bart Massey

Herein lie Rust solutions to day one through part 1 of day
nine of the 2022
[Advent of Code](http://adventofcode.com). The solutions
will stop when the fun stops: This is the second time Bart
got stuck on a hard-to-find bug.

We were working mostly in pair-programming mode, with one of
us taking the lead on each problem. Occasionally, we worked
a problem independently and compared solutions.

## Organization

The solutions are in directories named `day01`, `day02`,
etc. Each day is its own Git submodule. When you clone
this repo, you will need to do

    git submodule update --init

For each solution, we include cleaned-up Rust code. There is
a `README.md` in every problem directory containing
algorithm descriptions, comments and usage instructions. (We
used to included the problem descriptions and my specific
`input.txt`, but apparently the authors of AoC don't want us
to do that.)

Solutions load library code from the
[`libaoc` crate](https://github.com/BartMassey/libaoc). See
its documentation for details.

## Code Quality

There are no special system tests written for this code
other than the ones provided as part of the problem ---
there are occasional unit tests. We regard passing both parts
of a day's problem as strong validation, although we've been
wrong about this in the past. More tests should get written.

These programs are not production-quality: it is often
considered acceptable to panic on erroneous input.

## Goals

The goals of these solutions are to:

* Provide correct solutions with reasonable runtimes.

* Illustrate reasonable solution strategies.

* Illustrate the use of Rust in problem-solving.

As always we expect to learn some Rust and a little bit of
software engineering we should already have known writing
these.

## Infrastructure

There's some engineering infrastructure here in the form of
the `template` directory and the `mkday.sh` and other shell
scripts.  These speed each day's setup considerably. At the
beginning of each day we `sh mkday.sh`. (The day number is
tracked automatically but can be overwritten on the command
line.)

You can get times for all parts of all days with `sh
times.sh` (will build before timing). This also verifies
that everything runs.  This is a Rust workspace: you can use
Cargo commands at top-level on the entire workspace. `cargo
clean` is especially useful here — Rust `target` directories
are huge.

## Misc

These solutions deserve a much more thorough top-level
description than we usually have the energy to
write. Apologies.

## Previously

* [2020](http://github.com/BartMassey/advent-of-code-2020)
  in Rust (incomplete)
* [2019](http://github.com/BartMassey/advent-of-code-2019)
  in Rust (incomplete)
* [2018](http://gitlab.com/BartMassey/advent-of-code-2018)
  in Javascript (incomplete)
* [2017](http://gitlab.com/BartMassey/advent-of-code-2017)
  in Go
* [2016](http://github.com/BartMassey/advent-of-code-2016)
  in Rust
* [2015](http://github.com/BartMassey/advent-of-code-2015)
  in Haskell

## License

This work is licensed under the "MIT License".  Please see
the file `LICENSE` in the source distribution of this
software for license terms.

## Acknowledgments

Advent of Code is a fun exercise up to a point, and we thank
the author and others involved for their work. Thanks also
to `relsqui` for pointing us at this back in 2015.


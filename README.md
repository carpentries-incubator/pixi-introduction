# Introduction to Pixi

This repository contains a Carpentries format lesson covering technologies and best practices for reproducible scientific workflows.
The lesson has been designed to be taught over a one-day workshop, with the day divided into a half-day of instruction from the lesson material, and then a second half-day focusing on applying the lesson content to real world research applications to participants' research projects through interactive work sessions with the instruction team.

The content of the lesson is aimed at a target audience of students and professional researchers who already have at least some experience with software development, including file system structures, such as the Filesystem Hierarchy Standard of Unix-like systems, version control software, such as Git, and programming languages, such as Python or C++.

## Using the lesson

To step through the lesson, please follow it on its website at https://carpentries-incubator.github.io/pixi-introduction/

## Getting help

* If you have questions about the lesson content or if something seems unclear, please open a [GitHub Discussion](https://github.com/carpentries-incubator/pixi-introduction/discussions).
GitHub Discussions that can not be resolved will be converted into GitHub Issues to be followed up on.
* If you have failed to reproduce results in the lesson content, or have found a bug, or something conceptually wrong, please open a [GitHub Issue](https://github.com/carpentries-incubator/pixi-introduction/issues).

## Contributing

Contributions to the lesson are welcome.
Before starting any work on a contribution idea, please first review the [Code of Conduct](https://github.com/carpentries-incubator/pixi-introduction/blob/main/CODE_OF_CONDUCT.md) and the [`CONTRIBUTING.md`](https://github.com/carpentries-incubator/pixi-introduction/blob/main/CONTRIBUTING.md).

## Developing the lesson

Similar to the lesson itself, development of the lesson uses [Pixi](https://pixi.sh/) to have unified multi-platform reproducible environments.
To start developing:

1. [Install Pixi](https://pixi.sh/)
2. [Fork this repository on GitHub](https://github.com/carpentries-incubator/pixi-introduction/fork)
3. Clone your fork and navigate to the top level of the repository
4. Run

```
pixi run start
```

and then open up the served site in your local browser and carry on with development.

> [!TIP]
> This lesson uses [The Carpentries Workbench][workbench].
> Consider reviewing The Workbench documentation and [infrastructure][] before starting development.

[workbench]: https://carpentries.github.io/sandpaper-docs/
[infrastructure]: https://carpentries.github.io/workbench/

# PIECE
PIECE analysis.

<!-- TOC -->

- [PIECE](#piece)
- [Introduction](#introduction)
- [Things to learn and research](#things-to-learn-and-research)
- [Before you start](#before-you-start)
- [Lab Exercises](#lab-exercises)
- [Project structure](#project-structure)

<!-- /TOC -->
---
# Introduction

Lab exercises to perform PIECE analysis. PIECE is an acronym for:
* Profitability - measured in earnings per share
* Inflow of cash - measured in operating cashflow
* Efficiency - measured in return on equity
* Conservative debt - measured in debt to equity
* Evaluation - estimated target price

---
# Things to learn and research
In no particular order, my plan is to use the following resources to learn and research.

| Title | Type | Author |
|-----|-----|-----|
| [OpenBB-finance/OpenBBTerminal: Investment Research for Everyone, Anywhere.](https://github.com/OpenBB-finance/OpenBBTerminal) | GitHub Repo | OpenBB-finance |

---
# Before you start

Before proceeding any further, make sure you have completed the required setup steps described by the links below:
* Download and install [Docker Desktop](https://www.docker.com/products/docker-desktop).
* Open a terminal and run OpenBB with the following command:

```sh
docker run -it --rm ghcr.io/openbb-finance/openbbterminal-poetry:latest
```

---
# Lab Exercises
- [ ] [Lab 01. - Hello Apple](./lab/01-hello-apple/LAB-01.md#table-of-contents)

---
# Project structure

```
piece/                            <-- Root of your Project
|- .gitignore                     <-- GitHub ignore
|- README.md                      <-- GitHub README markdown
   +- lab/                        <-- Holds any lab exercises
```

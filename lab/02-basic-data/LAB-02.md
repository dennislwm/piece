# Table of contents

<!-- TOC -->

- [Table of contents](#table-of-contents)
- [Introduction](#introduction)
- [Before you start](#before-you-start)
- [Lab 02 - Basic Data](#lab-02---basic-data)
  - [Exercise 1](#exercise-1)
  - [Exercise 2](#exercise-2)
  - [Challenging Exercise 3](#challenging-exercise-3)
- [Continue](#continue)

<!-- /TOC -->
---
# Introduction

Welcome to the second exercise on the PIECE analysis.

This document is a step-by-step guide to performing this exercise. The instructions should work equally well on Windows, macOS and Linux.

Even if you are familiar with basics, stepping through this guide may be helpful as it will help you understand the output from the tool, **OpenBB**, that we use to get our data and perform our analysis.

---
# Before you start

Before proceeding any further, make sure you have completed the required setup steps described by the links below:
* Download and install [Docker Desktop](https://www.docker.com/products/docker-desktop).
* Open a terminal and run OpenBB with the following command:

```sh
docker run -it --rm ghcr.io/openbb-finance/openbbterminal-poetry:latest
```

---
# Lab 02 - Basic Data

## Exercise 1
Get the basic data of Apple and fill in the table below.

| Company | Ticker | Last Price | Beta |
|----|----|----|----|
| Apple | AAPL | | |

<details>
<summary> Click here to <strong>get the basic data of Apple.</strong></summary><br>

Solution will be published soon.

> Explanation: 

</details>

## Exercise 2
Get the current valuation of Apple and fill in the table below.

| Market Cap (USD) | Price-to-Earnings (P/E) | Price-to-Book (P/B) | Dividend Yield (%) |
|----|----|----|----|
| $2,353 Bln | | | |

<details>
<summary> Click here to <strong>get the current valuation of Apple.</strong></summary><br>

Solution will be published soon.

> Explanation: 
</details>

## (Challenging) Exercise 3
Get the 52-week high and low price of Apple and fill in the table below.

| Last Price (USD) | Discount/Fair/Premium | 52W Low | 52W High |
|----|----|----|----|
| $147.07 | | | |

> Apply the following to determine if the Last Price is at a Discount/Fair/Premium price.
> - Discount: Last Price < 40% of the 52W range.
> - Fair: 40% of 52W range <= Last Price <= 60% of range
> - Premium: Last Price > 60% of the 52W range

<details>
<summary> Click here to <strong>get the 52W high and low price of Apple.</strong></summary><br>

Solution will be published soon.

> Explanation: 
</details>

---
# Continue

You have successfully completed this lab. Move on to the next lab.

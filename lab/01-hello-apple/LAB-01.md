# Table of contents

<!-- TOC -->

- [Table of contents](#table-of-contents)
- [Introduction](#introduction)
- [Before you start](#before-you-start)
- [Lab 01 - Hello Apple](#lab-01---hello-apple)
  - [Exercise 1](#exercise-1)
  - [Exercise 2](#exercise-2)
  - [Optional Exercise 3](#optional-exercise-3)
- [Continue](#continue)

<!-- /TOC -->
---
# Introduction

Welcome to the first exercise on the PIECE analysis.

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
# Lab 01 - Hello Apple

## Exercise 1
Get the stock price of Apple.

<details>
<summary> Click here to <strong>get the stock price of Apple.</strong></summary><br>

```
/ $ stocks
```
```
/stocks/ $ quote AAPL
```
```sh
         Ticker Quote          
┏━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━┓
┃                ┃ AAPL       ┃
┡━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━┩
│ Name           │ Apple Inc. │
├────────────────┼────────────┤
│ Price          │ 150.17     │
├────────────────┼────────────┤
│ Open           │ 149.78     │
├────────────────┼────────────┤
│ High           │ 150.86     │
├────────────────┼────────────┤
│ Low            │ 148.20     │
├────────────────┼────────────┤
│ Previous Close │ 148.47     │
├────────────────┼────────────┤
│ Volume         │ 75,396,045 │
├────────────────┼────────────┤
│ 52 Week High   │ 182.94     │
├────────────────┼────────────┤
│ 52 Week Low    │ 129.04     │
├────────────────┼────────────┤
│ Change         │ 1.70       │
├────────────────┼────────────┤
│ Change %       │ 1.15%      │
└────────────────┴────────────┘
```

> Explanation: The Open, High, Low, and previous Close [OHLC] prices are based on the last daily candle of the stock. The Volume shows the number of units traded, while Change and Change % shows the dollar and percent change in price of previous Close.

</details>

## Exercise 2
Get the EPS of Apple.

<details>
<summary> Click here to <strong>get the EPS of Apple.</strong></summary><br>

```
/stocks/ $ load AAPL
```
```sh
Loading Daily AAPL stock with starting period 2019-07-15 for analysis.

Datetime: 2022 Jul 16 23:06
Timezone: America/New_York
Currency: USD
Market:   CLOSED
```
```
/stocks/ $ fa
```
```
/stocks/fa $ data
```
```sh
               Ticker Screener                
┏━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━┓
┃                    ┃ Values                ┃
┡━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━┩
│ Company            │ Apple Inc.            │
├────────────────────┼───────────────────────┤
│ Sector             │ Technology            │
├────────────────────┼───────────────────────┤
│ Industry           │ Consumer Electronics  │
├────────────────────┼───────────────────────┤
│ Country            │ USA                   │
├────────────────────┼───────────────────────┤
│ Website            │ https://www.apple.com │
├────────────────────┼───────────────────────┤
│ Index              │ DJIA S&P500           │
├────────────────────┼───────────────────────┤
│ P/E                │ 24.41                 │
├────────────────────┼───────────────────────┤
│ EPS (ttm)          │ 6.15                  │
├────────────────────┼───────────────────────┤
│ Insider Own        │ 0.07%                 │
├────────────────────┼───────────────────────┤
│ Shs Outstand       │ 16.28B                │
├────────────────────┼───────────────────────┤
│ Perf Week          │ 2.13%                 │
├────────────────────┼───────────────────────┤
│ Market Cap         │ 2419.12B              │
├────────────────────┼───────────────────────┤
│ Forward P/E        │ 22.95                 │
├────────────────────┼───────────────────────┤
│ EPS next Y         │ 6.54                  │
├────────────────────┼───────────────────────┤
│ Insider Trans      │ -1.63%                │
├────────────────────┼───────────────────────┤
│ Shs Float          │ 16.17B                │
├────────────────────┼───────────────────────┤
│ Perf Month         │ 13.11%                │
├────────────────────┼───────────────────────┤
│ Income             │ 101.94B               │
├────────────────────┼───────────────────────┤
│ PEG                │ 2.46                  │
├────────────────────┼───────────────────────┤
│ EPS next Q         │ 1.16                  │
├────────────────────┼───────────────────────┤
│ Inst Own           │ 59.70%                │
├────────────────────┼───────────────────────┤
│ Short Float        │ 0.70%                 │
├────────────────────┼───────────────────────┤
│ Perf Quarter       │ -11.87%               │
├────────────────────┼───────────────────────┤
│ Sales              │ 386.02B               │
├────────────────────┼───────────────────────┤
│ P/S                │ 6.27                  │
├────────────────────┼───────────────────────┤
│ EPS this Y         │ 71.40%                │
├────────────────────┼───────────────────────┤
...
```
> Explanation: Earnings per share [EPS] measures the profitability of a company. The stronger the profitability, the higher the EPS.

> The data returned has multiple 'EPS' entries. The main difference between these is the length of period used to determine the earnings. For example, `ttm` uses the trailing 12-month period to calculate the earnings.
</details>

## (Optional) Exercise 3
Search for other `apple` stocks.

<details>
<summary> Click here to <strong>search for other apple stocks.</strong></summary><br>

```
/stocks/ $ search apple
```
```sh
               Search Results               
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━┓
┃ Company                         ┃ Ticker ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━┩
│ Apple Inc.                      │ AAPL   │
├─────────────────────────────────┼────────┤
│ APPLE GREEN HOLDING INC         │ AGPL   │
├─────────────────────────────────┼────────┤
│ Apple Hospitality REIT, Inc.    │ APLE   │
├─────────────────────────────────┼────────┤
│ APPLE RUSH COMPANY INC          │ APRU   │
├─────────────────────────────────┼────────┤
│ GOLDEN APPLE OIL & GAS INC      │ GAPJ   │
├─────────────────────────────────┼────────┤
│ Maui Land & Pineapple Company,  │ MLP    │
├─────────────────────────────────┼────────┤
│ PINEAPPLE EXPRESS INC           │ PNPL   │
└─────────────────────────────────┴────────┘
```
> Explanation: The search function will lookup your search term, e.g. 'apple', in the company name. You can then reference the **`Ticker`** to get additional information about the company.
</details>

---
# Continue

You have successfully completed this lab. Move on to the next lab.

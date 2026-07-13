# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

# 学习背景

## 身份
大一学生，信工+机械交叉方向，目标学习算法/Embodied AI。

## 开发环境
- Anaconda + VS Code + Jupyter Notebook
- conda 环境名：d2l（Python 3.10）
- PyTorch 2.11，RTX 5050 GPU
- 项目目录：~/OneDrive/Desktop/Deep learning/D2L

## 当前学习进度
正在学习《动手学深度学习》（d2l），PyTorch 版本。

已完成：
- 第 2 章全部（数据操作、数据预处理、线性代数、微积分、自动微分、概率）
- 第 3.1 节（线性回归理论）

当前：第 3.2 节（线性回归从零开始实现）

## Python 基础
已掌握：列表、字典、函数、OOP、NumPy、张量操作、自动微分

## 教学要求
1. 解释代码时逐行讲清楚，不要跳过细节
2. 遇到数学公式用通俗语言解释含义
3. 报错直接告诉我原因和修复方法
4. 练习题直接讲解，不需要等我先写
5. 回答简洁，有错误才展开讲

## Project Overview

This is a personal D2L (Dive into Deep Learning) study repository. Notebooks are written in Chinese with PyTorch as the backend.

## Structure

Notebooks are organized by chapter: `Ch02/` covers prerequisites (tensors, calculus, probability), `Ch03/` covers linear regression. Each notebook filename maps to a D2L section (e.g., `ch03_01_线性回归.ipynb`).

## Key Libraries

- `torch` — primary tensor/model library
- `numpy` / `matplotlib` — numerical ops and plotting
- `d2l` (from `d2l import torch as d2l`) — D2L helper library; use `d2l.plot(...)` for multi-curve plots and `d2l.plt` to access the underlying `matplotlib.pyplot` for post-plot customization (e.g., `d2l.plt.axhline(...)`)

## Editing Notebooks

- Always **save the file in the IDE before asking Claude to read it** — unsaved changes are not visible on disk
- When editing a cell, the IDE must not save over the file between Claude's read and write; if it does, the edit will be silently overwritten
- Use `NotebookEdit` with the `cell_id` shown in Read output to target a specific cell
- `d2l.plot` clears the axes (`axes.cla()`), so any additional plot calls (e.g., `axhline`) must come **after** `d2l.plot`

## Plotting Conventions

- Inline backend: `%matplotlib inline` at the top of each notebook
- Multi-curve plots use `d2l.plot(x, [y1, y2, ...], xlabel=..., ylabel=..., legend=[...])`
- To add elements after `d2l.plot`, use `d2l.plt.<method>` (e.g., `d2l.plt.axhline(y=0, color='black', linestyle='-')`)

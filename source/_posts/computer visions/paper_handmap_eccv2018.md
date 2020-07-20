---
title: HandMap: Robust Hand Pose Estimation via Intermediate Dense Guidance Map Supervision
date: 2020/7/17 16:02
toc: true
categories:
- computer visions
tags:
- computer visions
- tensorflow
- paper
---





## Distance Transform

> ref: https://medium.com/on-coding/euclidean-distance-transform-d37e06958216

最简单的 Distance transform 把二值图像作为输入，输出每一个点到 **最近的** 白色像素的欧式距离。

对于一般图像来说，做 Distance Transform 前需要二值化。

![1 b7gJ0Z-_RT3At_u96t1DPQ](img/paper_handmap_eccv2018/1 b7gJ0Z-_RT3At_u96t1DPQ.gif)

> 这匹马就是二值化后做 Distance Transform 的



解决这个问题最复杂的是，如何快速找到最近的白色像素点。
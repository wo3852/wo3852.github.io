---
title: 행렬의 덧셈
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "행렬의 덧셈" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

행렬의 덧셈은 행과 열의 크기가 같은 두 행렬의 같은 행, 같은 열의 값을 서로 더한 결과가 됩니다. 2개의 행렬 arr1과 arr2를 입력받아, 행렬 덧셈의 결과를 반환하는 함수, solution을 완성해주세요.

>**제한 조건**


행렬 arr1, arr2의 행과 열의 길이는 500을 넘지 않습니다.


>**입출력 예**

| arr1 | arr2 | return |
|--|--|--|
| [[1,2],[2,3]] | [[3,4],[5,6]] | [[4,6],[7,9]] |
| [[1],[2]] | [[3],[4]] | [[4],[6]] |

>**문제 풀이**

	def solution(arr1, arr2): return [[a+b for a,b in zip(a1,a2)] for a1,a2 in zip(arr1,arr2)]




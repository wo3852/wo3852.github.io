---
title: 행렬의 곱셈 (Python)
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "행렬의 곱셈" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

2차원 행렬 arr1과 arr2를 입력받아, arr1에 arr2를 곱한 결과를 반환하는 함수, solution을 완성해주세요.

>**제한 조건**


행렬 arr1, arr2의 행과 열의 길이는 2 이상 100 이하입니다.
행렬 arr1, arr2의 원소는 -10 이상 20 이하인 자연수입니다.
곱할 수 있는 배열만 주어집니다.


>**입출력 예**

| arr1 | arr2 | return |
|--|--|--|
| [[1, 4], [3, 2], [4, 1]] | [[3, 3], [3, 3]] | [[15, 15], [15, 15], [15, 15]] |
| [[2, 3, 2], [4, 2, 4], [3, 1, 4]] | [[5, 4, 3], [2, 4, 1], [3, 1, 1]] | [[22, 22, 11], [36, 28, 18], [29, 20, 14]] |

>**문제 풀이**

	def solution(arr1, arr2):
	  answer = [[0 for _ in range(len(arr2[0]))] for _ in range(len(arr1))]
	  for i in range(len(arr1)):
	    for j in range(len(arr2[0])):
	      for h in range(len(arr1[0])):answer[i][j] += arr1[i][h]*arr2[h][j]
	  return answer


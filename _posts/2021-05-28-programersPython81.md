---
title: 정수 내림차순으로 배치하기 (Python)
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "정수 내림차순으로 배치하기" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

함수 solution은 정수 n을 매개변수로 입력받습니다. n의 각 자릿수를 큰것부터 작은 순으로 정렬한 새로운 정수를 리턴해주세요. 예를들어 n이 118372면 873211을 리턴하면 됩니다.

>**제한 조건**


 n 은 1이상 8000000000 이하인 자연수입니다.


>**입출력 예**

| n | return |
|--|--|
| 118372 | 873211 |

>**문제 풀이**

	def solution(n):
	  return int("".join(sorted([i for i in str(n)],reverse=True)))




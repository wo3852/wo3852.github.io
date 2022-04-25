---
title: 자연수 뒤집어 배열로 만들기 (Python)
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "자연수 뒤집어 배열로 만들기" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

자연수 n을 뒤집어 각 자리 숫자를 원소로 가지는 배열 형태로 리턴해주세요. 예를들어 n이 12345이면 [5,4,3,2,1]을 리턴합니다.

>**제한 조건**


n은 10,000,000,000이하인 자연수입니다.


>**입출력 예**

| n | return |
|--|--|
| 12345 | [5,4,3,2,1] |

>**문제 풀이**

	def solution(n):
	  return [int(i) for i in list(reversed(str(n)))]




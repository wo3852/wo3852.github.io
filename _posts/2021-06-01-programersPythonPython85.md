---
title: 짝수와 홀수 (Python)
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "짝수와 홀수" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

정수 num이 짝수일 경우 "Even"을 반환하고 홀수인 경우 "Odd"를 반환하는 함수, solution을 완성해주세요.

>**제한 조건**


num은 int 범위의 정수입니다.
0은 짝수입니다.


>**입출력 예**

| num | return |
|--|--|
| 3 | "Odd" |
| 4 | "Even" |

>**문제 풀이**

	def solution(num): return "Even" if num%2 == 0 else "Odd"




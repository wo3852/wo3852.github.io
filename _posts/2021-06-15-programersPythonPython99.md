---
title: 직사각형 별찍기
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "직사각형 별찍기" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

이 문제에는 표준 입력으로 두 개의 정수 n과 m이 주어집니다.
별(*) 문자를 이용해 가로의 길이가 n, 세로의 길이가 m인 직사각형 형태를 출력해보세요.

>**제한 조건**

<ul>
<li>n과 m은 각각 1000 이하인 자연수입니다.</li>
</ul>

>**예시**

입력

5 3

출력

"*****"

"*****"

"*****"

>**문제 풀이**

	n, m = map(int, input().strip().split(' '))
	for i in range(m):
	  for j in range(n):
	    print("*",end="")
	  print()


---
title: 숫자의 표현
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "숫자의 표현" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

Finn은 요즘 수학공부에 빠져 있습니다. 수학 공부를 하던 Finn은 자연수 n을 연속한 자연수들로 표현 하는 방법이 여러개라는 사실을 알게 되었습니다. 예를들어 15는 다음과 같이 4가지로 표현 할 수 있습니다.

<ul>
<li>1 + 2 + 3 + 4 + 5 = 15</li>
<li>4 + 5 + 6 = 15</li>
<li>7 + 8 = 15</li>
<li>15 = 15</li>
</ul>

자연수 n이 매개변수로 주어질 때, 연속된 자연수들로 n을 표현하는 방법의 수를 return하는 solution를 완성해주세요.

>**제한사항**



>**입출력 예**

| n | result |
|--|--|
| 15 | 4 |


>**입출력 예 설명**

<ul>
<li>n은 10,000 이하의 자연수 입니다.</li>
</ul>

>**문제 풀이**

	def solution(n):
	  if n == 0: return 0
	  answer = 1
	  last = int(n/2) if n/2 == int(n/2) else int(n/2)+1
	  a = 2 if n/2 == int(n/2) else 1
	  temp = [i for i in range(1,last+1)]
	  start = 0
	  while start != len(temp)-a:
	    for i in range(start+1,len(temp)+1):
	      Sum = sum(temp[start:i])
	      if Sum == n:
	        answer += 1
	        start +=1
	        break
	      elif Sum > n:
	        start +=1
	        break
	  return answer



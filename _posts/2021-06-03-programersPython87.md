---
title: 최대공약수와 최소공배수 (Python)
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "최대공약수와 최소공배수" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

두 수를 입력받아 두 수의 최대공약수와 최소공배수를 반환하는 함수, solution을 완성해 보세요. 배열의 맨 앞에 최대공약수, 그다음 최소공배수를 넣어 반환하면 됩니다. 예를 들어 두 수 3, 12의 최대공약수는 3, 최소공배수는 12이므로 solution(3, 12)는 [3, 12]를 반환해야 합니다.

>**제한 사항**


두 수는 1이상 1000000이하의 자연수입니다.


>**입출력 예**

| n | m | return |
|--|--|--|
| 3 | 12 | [3, 12] |
| 2 | 5 | [1, 10] |

>**입출력 예 설명**

입출력 예 #1

위의 설명과 같습니다.

입출력 예 #2

자연수 2와 5의 최대공약수는 1, 최소공배수는 10이므로 [1, 10]을 리턴해야 합니다.

>**문제 풀이**

	def solution(n, m):
	  list = sorted([n,m])
	  answer = []
	  temp = list[:]
	  for i in range(list[0],0,-1):
	    if list[0] % i == 0 and list[1] % i == 0:
	      answer.append(i)
	      break
	  while True:
	    if list[0] < list[1] : list[0] += temp[0]
	    elif list[0] > list[1] : list[1] += temp[1]
	    else : return answer+[list[0]]




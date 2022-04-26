---
title: 타겟 넘버 (Python)
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "타겟 넘버" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

n개의 음이 아닌 정수들이 있습니다. 이 정수들을 순서를 바꾸지 않고 적절히 더하거나 빼서 타겟 넘버를 만들려고 합니다. 예를 들어 [1, 1, 1, 1, 1]로 숫자 3을 만들려면 다음 다섯 방법을 쓸 수 있습니다.

    -1+1+1+1+1 = 3
    +1-1+1+1+1 = 3
    +1+1-1+1+1 = 3
    +1+1+1-1+1 = 3
    +1+1+1+1-1 = 3

사용할 수 있는 숫자가 담긴 배열 numbers, 타겟 넘버 target이 매개변수로 주어질 때 숫자를 적절히 더하고 빼서 타겟 넘버를 만드는 방법의 수를 return 하도록 solution 함수를 작성해주세요.

>**제한사항**


주어지는 숫자의 개수는 2개 이상 20개 이하입니다.
각 숫자는 1 이상 50 이하인 자연수입니다.
타겟 넘버는 1 이상 1000 이하인 자연수입니다.


>**입출력 예**

| numbers | target | return |
|--|--|--|
| [1, 1, 1, 1, 1] | 3 | 5 |
| [4, 1, 2, 1] | 4 | 2 |

>**입출력 예 설명**

입출력 예 #1

문제 예시와 같습니다.

입출력 예 #2

    +4+1-2+1 = 4
    +4-1+2-1 = 4


총 2가지 방법이 있으므로, 2를 return 합니다.


>**문제 풀이**

	from itertools import combinations
	def solution(numbers, target):
	  answer = 0
	  rang = list(range(len(numbers)))
	  for i in range(1,len(numbers)+1):
	    temp = list(combinations(rang,i))
	    for j in temp:
	      num = numbers[:]
	      for h in j:num[h] = -num[h]
	      if sum(num) == target:answer+=1
	  return answer



---
title: 없는 숫자 더하기 (Python)
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "없는 숫자 더하기" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

0부터 9까지의 숫자 중 일부가 들어있는 정수 배열 numbers가 매개변수로 주어집니다. numbers에서 찾을 수 없는 0부터 9까지의 숫자를 모두 찾아 더한 수를 return 하도록 solution 함수를 완성해주세요.

>**제한사항**


1 ≤  numbers 의 길이 ≤ 9


0 ≤  numbers 의 모든 원소 ≤ 9
 numbers 의 모든 원소는 서로 다릅니다.



>**입출력 예**

| numbers | result |
|--|--|
| [1,2,3,4,6,7,8,0] | 14 |
| [5,8,4,0,6,7,9] | 6 |

>**입출력 예 설명**

입출력 예 #1


5, 9가  numbers 에 없으므로, 5 + 9 = 14를 return 해야 합니다.


입출력 예 #2


1, 2, 3이  numbers 에 없으므로, 1 + 2 + 3 = 6을 return 해야 합니다.


>**문제 풀이**

	def solution(numbers):
	  return sum([i for i in range(1,10) if numbers.count(i) == 0])




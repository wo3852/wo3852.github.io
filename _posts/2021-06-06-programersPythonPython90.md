---
title: 평균 구하기
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "평균 구하기" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

정수를 담고 있는 배열 arr의 평균값을 return하는 함수, solution을 완성해보세요.

>**제한사항**

<ul>
<li>arr은 길이 1 이상, 100 이하인 배열입니다.</li>
<li>arr의 원소는  -10,000 이상 10,000 이하인 정수입니다.</li>
</ul>

>**입출력 예**

| arr | return |
|--|--|
| [1,2,3,4] | 2.5 |
| [5,5] | 5 |

>**문제 풀이**

	def solution(arr): return sum(arr)/len(arr)




---
title: 주식가격
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "주식가격" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

초 단위로 기록된 주식가격이 담긴 배열 prices가 매개변수로 주어질 때, 가격이 떨어지지 않은 기간은 몇 초인지를 return 하도록 solution 함수를 완성하세요.

>**제한사항**

<ul>
<li>prices의 각 가격은 1 이상 10,000 이하인 자연수입니다.</li>
<li>prices의 길이는 2 이상 100,000 이하입니다.</li>
</ul>

>**입출력 예**

| prices | return |
|--|--|
| [1, 2, 3, 2, 3] | [4, 3, 1, 1, 0] |

>**입출력 예 설명**

<ul>
<li>1초 시점의 ₩1은 끝까지 가격이 떨어지지 않았습니다.</li>
<li>2초 시점의 ₩2은 끝까지 가격이 떨어지지 않았습니다.</li>
<li>3초 시점의 ₩3은 1초뒤에 가격이 떨어집니다. 따라서 1초간 가격이 떨어지지 않은 것으로 봅니다.</li>
<li>4초 시점의 ₩2은 1초간 가격이 떨어지지 않았습니다.</li>
<li>5초 시점의 ₩3은 0초간 가격이 떨어지지 않았습니다.</li>
</ul>

>**문제 풀이**

	def solution(prices):
	  answer = [0] * len(prices)
	  def check():
	    count = 1
	    for j in range(i+1,len(prices)-1):
	      if prices[i] > prices[j]:
	        answer[i] = count
	        return
	      else: count+=1
	    answer[i] = count
	  for i in range(len(prices)-1):
	    check()
	  return answer

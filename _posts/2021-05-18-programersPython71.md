---
title: 문자열 다루기 기본 (Python)
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "문자열 다루기 기본" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

문자열 s의 길이가 4 혹은 6이고, 숫자로만 구성돼있는지 확인해주는 함수, solution을 완성하세요. 예를 들어 s가 "a234"이면 False를 리턴하고 "1234"라면 True를 리턴하면 됩니다.

>**제한 사항**


 s는 길이 1 이상, 길이 8 이하인 문자열입니다.


>**입출력 예**

| s | return |
|--|--|
| "a234" | false |
| "1234" | true |

>**문제 풀이**

	def solution(s):
	  return s.isdigit() if len(s) == 4 or len(s) == 6 else False




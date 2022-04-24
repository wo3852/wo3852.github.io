---
title: 가운데 글자 가져오기
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "가운데 글자 가져오기" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

단어 s의 가운데 글자를 반환하는 함수, solution을 만들어 보세요. 단어의 길이가 짝수라면 가운데 두글자를 반환하면 됩니다.

>**재한사항**


s는 길이가 1 이상, 100이하인 스트링입니다.


>**입출력 예**

| s | return |
|--|--|
| "abcde" | "c" |
| "qwer" | "we" |

>**문제 풀이**

	def solution(s):
	  return s[int((len(s)-1)/2)] if int(len(s)%2) == 1 else s[int((len(s)-1)/2):int((len(s))/2)+1]


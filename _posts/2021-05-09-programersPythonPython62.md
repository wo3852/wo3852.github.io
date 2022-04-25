---
title: 올바른 괄호
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "올바른 괄호" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

괄호가 바르게 짝지어졌다는 것은 '(' 문자로 열렸으면 반드시 짝지어서 ')' 문자로 닫혀야 한다는 뜻입니다. 예를 들어


"()()" 또는 "(())()" 는 올바른 괄호입니다.
")()(" 또는 "(()(" 는 올바르지 않은 괄호입니다.


'(' 또는 ')' 로만 이루어진 문자열 s가 주어졌을 때, 문자열 s가 올바른 괄호이면 true를 return 하고, 올바르지 않은 괄호이면 false를 return 하는 solution 함수를 완성해 주세요.

>**제한사항**


문자열 s의 길이 : 100,000 이하의 자연수
문자열 s는 '(' 또는 ')' 로만 이루어져 있습니다.


>**입출력 예**

| s | answer |
|--|--|
| "()()" | true |
| "(())()" | true |
| ")()(" | false |
| "(()(" | false |

>**입출력 예 설명**

입출력 예 #1,2,3,4

문제의 예시와 같습니다.

>**문제 풀이**

	def solution(s):
	  if len(s) % 2 !=0:return False
	  elif s.count("(") != s.count(")"):return False
	  elif s[0] != "(" or s[-1] != ")":return False
	  stack = []
	  for i in s:
	    if stack == []: 
	      stack.append(i)
	      continue
	    if i == ")" and stack[-1] =="(":stack.pop()
	    else: stack.append(i)
	  if stack == []: return True
	  else: return False




---
title: 서울에서 김서방 찾기 (Python)
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "서울에서 김서방 찾기" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

String형 배열 seoul의 element중 "Kim"의 위치 x를 찾아, "김서방은 x에 있다"는 String을 반환하는 함수, solution을 완성하세요. seoul에 "Kim"은 오직 한 번만 나타나며 잘못된 값이 입력되는 경우는 없습니다.

>**제한 사항**


seoul은 길이 1 이상, 1000 이하인 배열입니다.
seoul의 원소는 길이 1 이상,  20 이하인 문자열입니다.
"Kim"은 반드시 seoul 안에 포함되어 있습니다.


>**입출력 예**

| seoul | return |
|--|--|
| ["Jane", "Kim"] | "김서방은 1에 있다" |

>**문제 풀이**

	def solution(seoul):
	  return "김서방은 "+str(seoul.index("Kim"))+"에 있다"




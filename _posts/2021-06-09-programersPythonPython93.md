---
title: 핸드폰 번호 가리기 (Python)
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "핸드폰 번호 가리기" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

프로그래머스 모바일은 개인정보 보호를 위해 고지서를 보낼 때 고객들의 전화번호의 일부를 가립니다.
전화번호가 문자열 phone_number로 주어졌을 때, 전화번호의 뒷 4자리를 제외한 나머지 숫자를 전부 *으로 가린 문자열을 리턴하는 함수, solution을 완성해주세요.

>**제한 조건**


phone_number는 길이 4 이상,  20이하인 문자열입니다.


>**입출력 예**

| phone_number | return |
|--|--|
| "01033334444" | "*******4444" |
| "027778888" | "*****8888" |

>**문제 풀이**

	def solution(phone_number): return ("*"*int(len(phone_number)-4))+(phone_number[len(phone_number)-4:])




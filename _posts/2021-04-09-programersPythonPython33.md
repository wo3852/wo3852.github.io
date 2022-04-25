---
title: 조이스틱
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "조이스틱" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

조이스틱으로 알파벳 이름을 완성하세요. 맨 처음엔 A로만 이루어져 있습니다.
ex) 완성해야 하는 이름이 세 글자면 AAA, 네 글자면 AAAA

조이스틱을 각 방향으로 움직이면 아래와 같습니다.

    ▲ - 다음 알파벳
    ▼ - 이전 알파벳 (A에서 아래쪽으로 이동하면 Z로)
    ◀ - 커서를 왼쪽으로 이동 (첫 번째 위치에서 왼쪽으로 이동하면 마지막 문자에 커서)
    ▶ - 커서를 오른쪽으로 이동 (마지막 위치에서 오른쪽으로 이동하면 첫 번째 문자에 커서)

예를 들어 아래의 방법으로 "JAZ"를 만들 수 있습니다.

    1 첫 번째 위치에서 조이스틱을 위로 9번 조작하여 J를 완성합니다.
    2 조이스틱을 왼쪽으로 1번 조작하여 커서를 마지막 문자 위치로 이동시킵니다.
    3 마지막 위치에서 조이스틱을 아래로 1번 조작하여 Z를 완성합니다.
    따라서 11번 이동시켜 "JAZ"를 만들 수 있고, 이때가 최소 이동입니다.

만들고자 하는 이름 name이 매개변수로 주어질 때, 이름에 대해 조이스틱 조작 횟수의 최솟값을 return 하도록 solution 함수를 만드세요.

>**제한 사항**


name은 알파벳 대문자로만 이루어져 있습니다.
name의 길이는 1 이상 20 이하입니다.


>**입출력 예**

| name | return |
|--|--|
| "JEROEN" | 56 |
| "JAN" | 23 |

>**문제 풀이**

	def solution(name):
	  count = 0
	  for i in name:
	    if ord(i) <= ord("N"): count += ord(i) - 65
	    else: count += 91 - ord(i) 
	  if name.count("A") ==0: return (len(name)-1)+count
	  co_list=[]
	  for x in range(len(name)):
	    temp = name[len(name)-1:x:-1]
	    for i in range(1,len(temp[:])+1):
	      if temp[-1] == "A":temp = temp[0:len(temp)-1]
	    co_list.append((len(name[:x+1])-1)*2+len(temp))
	  return count+min(co_list)





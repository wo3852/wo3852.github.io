---
title: 그대로 출력하기 2(Python)(구현)(문자열)
layout: post
post-image: 'https://ifh.cc/g/zjvJzN.jpg'
description: 백준 알고리즘의 문제 '그대로 출력하기 2' 문제풀이입니다.
tags:
- 알고리즘
- 백준알고리즘
- Python
---


>** 문제 **

입력 받은 대로 출력하는 프로그램을 작성하시오.

>** 입력 **

입력이 주어진다. 입력은 최대 100줄로 이루어져 있고, 알파벳 소문자, 대문자, 공백, 숫자로만 이루어져 있다. 각 줄은 100글자를 넘지 않으며, 빈 줄이 주어질 수도 있고, 각 줄의 앞 뒤에 공백이 있을 수도 있다.

>** 출력 **

입력받은 그대로 출력한다.

>** 예제 입력 1 **

	    Hello
	
	Baekjoon     
	   Online Judge    

>** 예제 출력 1 **

	    Hello
	
	Baekjoon     
	   Online Judge    

>** 문제풀이 **

	while True:
	  try:
	    print(input())
	  except:
	    break

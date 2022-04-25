---
title: 신고 결과 받기
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "신고 결과 받기" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- SQL
---


>**문제 설명**



>**문제 설명**



>**제한사항**



>**입출력 예**



>**입출력 예 설명**



>**제한시간 안내**



>**문제 풀이**

	def solution(id_list, report, k):
	  answer = [0]*len(id_list)
	  dic = {i:[] for i in id_list}
	  ban_dic = {i:0 for i in id_list}
	  report = set(report)
	  
	  for i in report:
	    x,y = i.split()
	    dic[x].append(y)
	    ban_dic[y] += 1
	  
	  for i in range(len(id_list)):
	    for j in dic[id_list[i]]:
	      if ban_dic[j] >= k:
	        answer[i] += 1    
	    
	  return answer


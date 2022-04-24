---
title: 더 맵게
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "더 맵게" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

매운 것을 좋아하는 Leo는 모든 음식의 스코빌 지수를 K 이상으로 만들고 싶습니다. 모든 음식의 스코빌 지수를 K 이상으로 만들기 위해 Leo는 스코빌 지수가 가장 낮은 두 개의 음식을 아래와 같이 특별한 방법으로 섞어 새로운 음식을 만듭니다.

섞은 음식의 스코빌 지수 = 가장 맵지 않은 음식의 스코빌 지수 + (두 번째로 맵지 않은 음식의 스코빌 지수 * 2)
Leo는 모든 음식의 스코빌 지수가 K 이상이 될 때까지 반복하여 섞습니다.
Leo가 가진 음식의 스코빌 지수를 담은 배열 scoville과 원하는 스코빌 지수 K가 주어질 때, 모든 음식의 스코빌 지수를 K 이상으로 만들기 위해 섞어야 하는 최소 횟수를 return 하도록 solution 함수를 작성해주세요.

>**제한 사항**

<ul>
<li>scoville의 길이는 2 이상 1,000,000 이하입니다.</li>
<li>K는 0 이상 1,000,000,000 이하입니다.</li>
<li>scoville의 원소는 각각 0 이상 1,000,000 이하입니다.</li>
<li>모든 음식의 스코빌 지수를 K 이상으로 만들 수 없는 경우에는 -1을 return 합니다.</li>
</ul>

>**입출력 예**

| scoville | K | return |
|--|--|--|
| [1, 2, 3, 9, 10, 12] | 7 | 2 |

>**입출력 예 설명**

<ol>
<li><p>스코빌 지수가 1인 음식과 2인 음식을 섞으면 음식의 스코빌 지수가 아래와 같이 됩니다.<br>
새로운 음식의 스코빌 지수 = 1 + (2 * 2) = 5<br>
가진 음식의 스코빌 지수 = [5, 3, 9, 10, 12]</p></li>
<li><p>스코빌 지수가 3인 음식과 5인 음식을 섞으면 음식의 스코빌 지수가 아래와 같이 됩니다.<br>
새로운 음식의 스코빌 지수 = 3 + (5 * 2) = 13<br>
가진 음식의 스코빌 지수 = [13, 9, 10, 12]</p></li>
</ol>

>**문제 풀이**

	import heapq
	​
	def solution(scoville, K):
	  answer = 0
	  heapq.heapify(scoville)
	  while scoville[0] < K:
	    if len(scoville) <= 1: return -1
	    heapq.heappush(scoville, heapq.heappop(scoville) + (heapq.heappop(scoville) * 2))
	    answer += 1
	  return answer




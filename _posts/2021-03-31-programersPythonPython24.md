---
title: 거리두기 확인하기 (Python)
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "거리두기 확인하기" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

개발자를 희망하는 죠르디가 카카오에 면접을 보러 왔습니다.

코로나 바이러스 감염 예방을 위해 응시자들은 거리를 둬서 대기를 해야하는데 개발 직군 면접인 만큼
아래와 같은 규칙으로 대기실에 거리를 두고 앉도록 안내하고 있습니다.


대기실은 5개이며, 각 대기실은 5x5 크기입니다.
거리두기를 위하여 응시자들 끼리는 맨해튼 거리<sup id="fnref1"><a href="#fn1">1</a></sup>가 2 이하로 앉지 말아 주세요.
단 응시자가 앉아있는 자리 사이가 파티션으로 막혀 있을 경우에는 허용합니다.


예를 들어,

<img src="https://grepp-programmers.s3.ap-northeast-2.amazonaws.com/files/production/8c056cac-ec8f-435c-a49a-8125df055c5e/PXP.png" title="" alt="PXP.png">

위 그림처럼 자리 사이에 파티션이 존재한다면 맨해튼 거리가 2여도 거리두기를 지킨 것입니다.

<img src="https://grepp-programmers.s3.ap-northeast-2.amazonaws.com/files/production/d611f66e-f9c4-4433-91ce-02887657fe7f/PX_XP.png" title="" alt="PX_XP.png">

위 그림처럼 파티션을 사이에 두고 앉은 경우도 거리두기를 지킨 것입니다.

<img src="https://grepp-programmers.s3.ap-northeast-2.amazonaws.com/files/production/ed707158-0511-457b-9e1a-7dbf34a776a5/PX_OP.png" title="" alt="PX_OP.png">

위 그림처럼 자리 사이가 맨해튼 거리 2이고 사이에 빈 테이블이 있는 경우는 거리두기를 지키지 않은 것입니다.

<img src="https://grepp-programmers.s3.ap-northeast-2.amazonaws.com/files/production/4c548421-1c32-4947-af9e-a45c61501bc4/P.png" title="" alt="P.png">

응시자가 앉아있는 자리(P)를 의미합니다.

<img src="https://grepp-programmers.s3.ap-northeast-2.amazonaws.com/files/production/ce799a38-668a-4038-b32f-c515b8701262/O.png" title="" alt="O.png">

빈 테이블(O)을 의미합니다.

<img src="https://grepp-programmers.s3.ap-northeast-2.amazonaws.com/files/production/91e8f98b-baeb-4f81-8cb6-5bafebebdcc7/X.png" title="" alt="X.png">

파티션(X)을 의미합니다.

5개의 대기실을 본 죠르디는 각 대기실에서 응시자들이 거리두기를 잘 기키고 있는지 알고 싶어졌습니다. 자리에 앉아있는 응시자들의 정보와 대기실 구조를 대기실별로 담은 2차원 문자열 배열 places가 매개변수로 주어집니다. 각 대기실별로 거리두기를 지키고 있으면 1을, 한 명이라도 지키지 않고 있으면 0을 배열에 담아 return 하도록 solution 함수를 완성해 주세요.

>**제한사항**


 places 의 행 길이(대기실 개수) = 5


 places 의 각 행은 하나의 대기실 구조를 나타냅니다.

 places 의 열 길이(대기실 세로 길이) = 5
 places 의 원소는  P , O , X 로 이루어진 문자열입니다.


places 원소의 길이(대기실 가로 길이) = 5
P 는 응시자가 앉아있는 자리를 의미합니다.
 O 는 빈 테이블을 의미합니다.
 X 는 파티션을 의미합니다.

입력으로 주어지는 5개 대기실의 크기는 모두 5x5 입니다.
return 값 형식


1차원 정수 배열에 5개의 원소를 담아서 return 합니다.
 places 에 담겨 있는 5개 대기실의 순서대로, 거리두기 준수 여부를 차례대로 배열에 담습니다.
각 대기실 별로 모든 응시자가 거리두기를 지키고 있으면 1을, 한 명이라도 지키지 않고 있으면 0을 담습니다.



>**입출력 예**

| places | result |
|--|--|
| [["POOOP", "OXXOX", "OPXPX", "OOXOX", "POXXP"], ["POOPX", "OXPXP", "PXXXO", "OXXXO", "OOOPP"], ["PXOPX", "OXOXP", "OXPOX", "OXXOP", "PXPOX"], ["OOOXX", "XOOOX", "OOOXX", "OXOOX", "OOOOO"], ["PXPXP", "XPXPX", "PXPXP", "XPXPX", "PXPXP"]] | [1, 0, 1, 1, 1] |

>**입출력 예 설명**

입출력 예 #1

첫 번째 대기실

| No. | 0 | 1 | 2 | 3 | 4 |
|--|--|--|--|--|--|
| 0 | P | O | O | O | P |
| 1 | O | X | X | O | X |
| 2 | O | P | X | P | X |
| 3 | O | O | X | O | X |
| 4 | P | O | X | X | P |


모든 응시자가 거리두기를 지키고 있습니다.


두 번째 대기실

| No. | 0 | 1 | 2 | 3 | 4 |
|--|--|--|--|--|--|
| 0 | P | O | O | P | X |
| 1 | O | X | P | X | P |
| 2 | P | X | X | X | O |
| 3 | O | X | X | X | O |
| 4 | O | O | O | P | P |


(0, 0) 자리의 응시자와 (2, 0) 자리의 응시자가 거리두기를 지키고 있지 않습니다.
(1, 2) 자리의 응시자와 (0, 3) 자리의 응시자가 거리두기를 지키고 있지 않습니다.
(4, 3) 자리의 응시자와 (4, 4) 자리의 응시자가 거리두기를 지키고 있지 않습니다.


세 번째 대기실

| No. | 0 | 1 | 2 | 3 | 4 |
|--|--|--|--|--|--|
| 0 | P | X | O | P | X |
| 1 | O | X | O | X | P |
| 2 | O | X | P | O | X |
| 3 | O | X | X | O | P |
| 4 | P | X | P | O | X |


모든 응시자가 거리두기를 지키고 있습니다.


네 번째 대기실

| No. | 0 | 1 | 2 | 3 | 4 |
|--|--|--|--|--|--|
| 0 | O | O | O | X | X |
| 1 | X | O | O | O | X |
| 2 | O | O | O | X | X |
| 3 | O | X | O | O | X |
| 4 | O | O | O | O | O |


대기실에 응시자가 없으므로 거리두기를 지키고 있습니다.


다섯 번째 대기실

| No. | 0 | 1 | 2 | 3 | 4 |
|--|--|--|--|--|--|
| 0 | P | X | P | X | P |
| 1 | X | P | X | P | X |
| 2 | P | X | P | X | P |
| 3 | X | P | X | P | X |
| 4 | P | X | P | X | P |


모든 응시자가 거리두기를 지키고 있습니다.


두 번째 대기실을 제외한 모든 대기실에서 거리두기가 지켜지고 있으므로, 배열 [1, 0, 1, 1, 1]을 return 합니다.

>**제한시간 안내**


정확성 테스트 : 10초




<li id="fn1">
<p>두 테이블 T1, T2가 행렬 (r1, c1), (r2, c2)에 각각 위치하고 있다면, T1, T2 사이의 맨해튼 거리는 |r1 - r2| + |c1 - c2| 입니다.&nbsp;<a href="#fnref1">↩</a></p>




>**문제 풀이**

	def solution(places):
	  answer = []
	  dx = [0,1,0,-1]
	  dy = [-1,0,1,0]
	  checkX = [[1,-1],[1],[1,-1],[-1]]
	  checkY = [[-1],[1,-1],[1],[1,-1]]
	  for i in range(5):
	    check = True
	    for y in range(5):
	      for x in range(5):
	        if places[i][y][x] == "P":
	          for h in range(4):
	            sx = x+dx[h]
	            sy = y+dy[h]
	            if sx < 0 or sy < 0 or sx >= 5 or sy >= 5:continue
	            if places[i][sy][sx] == "X":continue
	            if places[i][sy][sx] == "P":
	              check = False
	              answer.append(0)
	              break
	            if places[i][sy][sx] == "O":
	              if dy[h] == 0:
	                if not (sx+dx[h] < 0 or sx+dx[h] >= 5):
	                  if places[i][sy][sx+dx[h]] == "P":
	                    check = False
	                    answer.append(0)
	                    break
	                for j in checkY[h]:
	                  ty = sy+j
	                  if ty < 0 or ty >= 5:continue
	                  if places[i][ty][sx] == "P":
	                    check = False
	                    break
	              else:
	                if not (sy+dy[h] < 0 or sy+dy[h] >= 5):
	                  if places[i][sy+dy[h]][sx] == "P":
	                    check = False
	                    answer.append(0)
	                    break
	                for j in checkX[h]:
	                  tx = sx+j
	                  if tx < 0 or tx >= 5:continue 
	                  if places[i][sy][tx] == "P":
	                    check = False
	                    break
	            if not check:
	              answer.append(0)
	              break
	        if not check:break
	      if not check:break 
	    if check:answer.append(1)
	  return answer



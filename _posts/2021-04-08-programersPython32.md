---
title: 소수 찾기 (Python)
layout: post
post-image: 'https://ifh.cc/g/paXC3t.jpg'
description: 프로그래머스의 알고리즘 문제 "소수 찾기" 문제풀이입니다.
tags:
- 알고리즘
- 프로그래머스
- Python
---


>**문제 설명**

한자리 숫자가 적힌 종이 조각이 흩어져있습니다. 흩어진 종이 조각을 붙여 소수를 몇 개 만들 수 있는지 알아내려 합니다.

각 종이 조각에 적힌 숫자가 적힌 문자열 numbers가 주어졌을 때, 종이 조각으로 만들 수 있는 소수가 몇 개인지 return 하도록 solution 함수를 완성해주세요.

>**제한사항**


numbers는 길이 1 이상 7 이하인 문자열입니다.
numbers는 0~9까지 숫자만으로 이루어져 있습니다.
"013"은 0, 1, 3 숫자가 적힌 종이 조각이 흩어져있다는 의미입니다.


>**입출력 예**

| numbers | return |
|--|--|
| "17" | 3 |
| "011" | 2 |

>**입출력 예 설명**

예제 #1

[1, 7]으로는 소수 [7, 17, 71]를 만들 수 있습니다.

예제 #2

[0, 1, 1]으로는 소수 [11, 101]를 만들 수 있습니다.


11과 011은 같은 숫자로 취급합니다.


>**문제 풀이**

    from itertools import permutations
    import math
    def is_prime_number(x):
        for i in range(2, int(math.sqrt(x)) + 1):
            if x % i == 0 :return False
    return True 

    def solution(numbers):
        answer = 0
        li = []
        for i in range(1,len(numbers)+1):
            a = list(permutations(numbers,i))
            for j in a:
                n = int("".join(j))
                if n == 1 or n == 0:continue
                li.append(n)
        li = set(li)
        
        for i in li:
            if is_prime_number(i):
                answer+=1   
        return answer




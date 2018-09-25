# Github 마크다운 정리 및 git 사용법

# Github 마크다운

## 1.헤더(제목) 문법
먼저 헤더에 주로 쓰이는 html에서 h1~h6과 같이 쓰이는 #갯수로 나뉘는 제목에 쓰이는 문법이 있다.

사용방법은 다음과 같다.
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```
결과는
# h1
## h2
### h3
#### h4
##### h5
###### h6

## 2. 블록쿼티 문법
블록쿼티 문법은 쉽게 풀어쓰면 한글에서 들여쓰기 같은 존재다.

사용방법은 다음과 같다.
```
> 최상위 블록쿼티
>> 하위 블록쿼티
```
결과는
> 최상위 블록쿼티
>> 하위 블록쿼티

블록단위로 띄어서 보기 좋게 정렬되는 효과가 있으며 그 내부에서는 다른 markdown 문법도 사용가능하다

예시
> 블록문법
>> ### Hello, GitHub!

## 3. 리스트 문법

### 3.1. 순서있는 문법
```
1. 하나
2. 둘
3. 삼
```
숫자와 . 으로 연결된 조합을 쓴다.
1. 하나
2. 둘
3. 삼

여담이지만 작년에 깃허브를 처음 쓸대도 대두되었던 이야기지만 숫자를 중간에 다르게 해도 내림차순으로 된다.
```
1. 하나
3. 삼
2. 둘
```
1. 하나
3. 삼
2. 둘

### 3.2. 순서없는 문법 (기호 사용)
```
* 하나
    + 둘
        - 삼
```
위와같은 기호로 쓰인다.

* 하나
    + 둘
        - 삼
### 4. 수평선 (hr 태그)
```
* * *
***
*****
- - -
-----
```
모두 동일하다.
* * *
***
*****
- - -
-----

### 5. 하이퍼링크
```
syntax: [보여질이름](링크주소).
바로가기: [서동준의 Github](https://github.com/sReNcAt).
<주소>.
<http://https://github.com/sReNcAt>.
<srencat@naver.com>.
```
바로가기: [서동준의 Github](https://github.com/sReNcAt).
<http://https://github.com/sReNcAt>.
<srencat@naver.com>.

### 6. 폰트 조절
```
*하나의 별*
_하나의 언더바_
**두개의 별**
__두개의 언더바__
++밑줄++
~~중앙 가로줄~~
```
아스테리스크(별), 언더바 하나는 약간 bold체? 해야하나 italy체? 처럼 변하고.
두개는 강조가 된다 (흡사 <strong></strong>).
*하나의 별*.
_하나의 언더바_.
**두개의 별**.
__두개의 언더바__.
++밑줄++.
~~중앙 가로줄~~.

### 7.이미지
```
![Alt text](http://www.nyan.cat/cats/original.gif "냥캣").
```
라는 문법이 존재하나 특이하게 width와 height 조절이 불가능해 보통 <img> 태그를 주료쓴다.

![Alt text](http://www.nyan.cat/cats/original.gif "냥캣")


***
마크다운 

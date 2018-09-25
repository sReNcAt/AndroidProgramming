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
syntax: [보여질이름](링크주소)

바로가기: [서동준의 Github](https://github.com/sReNcAt)

<주소>

<http://https://github.com/sReNcAt>

<srencat@naver.com>
```
바로가기: [서동준의 Github](https://github.com/sReNcAt)

<http://https://github.com/sReNcAt>

<srencat@naver.com>

### 6. 폰트 조절
```
*하나의 별*

_하나의 언더바_

**두개의 별**

__두개의 언더바__

++밑줄++

~~중앙 가로줄~~
```
아스테리스크(별), 언더바 하나는 약간 bold체? 해야하나 italy체? 처럼 변하고

두개는 강조가 된다 (흡사 <strong></strong>)

*하나의 별*

_하나의 언더바_

**두개의 별**

__두개의 언더바__

++밑줄++

~~중앙 가로줄~~

### 7.이미지
```
![Alt text](http://www.nyan.cat/cats/original.gif "냥캣").
```
라는 문법이 존재하나 특이하게 width와 height 조절이 불가능해 보통 <img> 태그를 주료쓴다.

![Alt text](http://www.nyan.cat/cats/original.gif "냥캣")


***

# Git 명령어 정리

![Alt text](https://github.com/sReNcAt/AndroidProgramming/blob/master/%EC%A0%9C%EB%AA%A9%20%EC%97%86%EC%9D%8C.png?raw=true "git 실행")

우선 적으로 git repo관리를 위해 사용자 설정을 해줘야한다.
repo별 설정 조회는 각 .git이 생성된 폴더로 경로를 이동하여 하여야한다
> 전역 사용자
**git config --global user.name "이름"**
**git config --global user.email "메일주소"**

> repo별 사용자
**git config user.name "이름"**
**git config user.email "메일주소"**

user설정은 필수며 미입력시 commit 집계도 되지않고 누가 커밋시켯는지 모르게된다

다음은 설정 정보 조회다
> 전역 설정 조회
**git config --global --list**
> repo별 설정 조회
**git config --list**

> 저장소 초기화 (첫 설정)
**git init**

> 저장소 복제 (내려받기)
**git clone "저장소 URL"**

> 원격 저장소 추가하기
**git remote add "원격 저장소" "저장소 URL" ""**

> 새 파일 추가하거나 기존파일 스테이징과 커밋
**git add "파일"**
**git add -p "파일" "파일"**

**git commit -m "메세제"**

> 모든 변경사항 커밋
**git commit -m "메세지" -a"**

> 작업 트리 되돌리기
**git checkout HEAD "파일" "파일"**

> 스테이징된 기본사항 리셋
**git reset HEAD "파일" "파일"**

> 라스트 커밋 픽스
**git commit -m "메세지" --amend**

> 이전 커밋 수정하고 재활용하기
**git commit -C HEAD --amend**

위까지는 마스터에 적용되는사항이며 밑에는 브랜치에 관하여 적는다

> 브랜치 리스트
**git branch**

> 리모트 브랜치 리스트
**git branch -r**

> 로컬 및 리모트 모든 브랜치 리스트
**git branch -a**

> 현재 브랜치에서 새로운 브랜치 추가
**git branch "새 브랜치이름"**

> 다른 브랜치 체크아웃
**git checkout "브랜치"**

> 현재 브랜치에서 새로운 브랜치 생성후 체크아웃
**git checkout -b "새 브랜치이름"**

> 브랜치 복사하기 (덮어쓰기)
**git branch -f "기존브랜치" "새 브랜치"**

> 브랜치 이동 혹은 리네임
**git checkout -m "기존브랜치 "새 브랜치"**
>> 새 브랜치가 존재하지 않을경우
**git checkout -M "기존브랜치" "새 브랜치"**

> 브랜치 합치기
**git merge "브랜치"**

> 커밋하지 않고 합치기
**git merge --no-commit "브랜치"**

> 브랜치 삭제하기
**git branch -d "브랜치"**

로그

> 모든 로그보기
**git log**

> 변경사항과 함께 로그
****

> 특정 갯수의 로그 보기
**git log -숫자**
**git log -1**
위는 1개만 보이기

> 1달간의 커밋 로그
**git log -since="1hours"**

> 3일전까지의 커밋 로그
**git log --before="2days"**

> x개 이전의 커밋 보그
**git log -1 HEAD-x**
**git log -1 HEAD-1**
위는 1개이전

> 작업 트리와 인덱스 차이 보기
**git diff**

> 인덱스와 repo 차이점
**git diff --cached**

> 작업트리와 repo 차이점
**git diff HEAD**

> 파일 커밋정보 줄단위 보기
**git blame "파일"**

> 파일 복사,붙여넣기,이동정보 줄단위 보기
**git blame -M "파일"**

> 파일 이동과 원본파일 정보 줄단위로 보기
**git blame -C-C "파일"

> repo 복제시 마지막 x개 커밋만 포함하여 복제
**git clone --depth x "저장소 URL"**
**git clone --depth 100 "저장소 URL"**
위는 마지막 100개의 커밋만 포함

> origin 저장소에 합치지 않고 로컬 브랜치로 변경사항 가져오기
**git fetch**

> 리모트 저장소에 합치지 않고 지역 브랜치로 변경사항 가져오기
**git fetch "저장소 URL"**

> 리모트 저장소에서 변경사항 가져와 현재 브랜치에 합치기
**git pull "저장소 URL"**

> origin 저장소에서 변경사항 가져와 현재 로컬브랜치에 합치기
**git pull**

> 로컬 브랜치를 리모트 브랜치에 푸시
**git push <저장소 URL> <로컬 브랜치>:<리모트 브랜치>**

> 로컬 브랜치를 동일한 이름의 리모트 브랜치에 푸시
**git push <저장소 URL> <로컬 브랜치>**

>새로운 로컬 브랜치를 리모트 저장소에 푸시
**git push <저장소 URL> <로컬 브랜치>**

>원격 저장소에서 쓸모가 없어진 원격 브랜치 제거하기
**git remote prune <저장소 URL>**

>원격 저장소를 제거하고 관련된 브랜치도 제거하기
**git remote rm <저장소 URL>**

#2018-09-26 AM03:42 Last Modify

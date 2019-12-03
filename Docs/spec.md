---
#About this file
title: "tangtangGames specification"
date: "2019-12-02"
category: "사양서"
edit_log: [
  {date : "2019-12-02", 
    participant: [ "CGM753", "lkoiescg2031" ],
    description: "최초 기획: 최초 기획 생성"
  },
  {date : "2019-12-03", 
    participant: [ "CGM753", "lkoiescg2031" ],
    description: "기획: 게임 설정"
  },
]
---

# 개요

참여자 : CGM753, lkoiescg2031
작성자 : lkoiescg2031

게임 개발에 관한 전반적 내용을 기록한 문서

editing log : 
2019-11-30 최초 회의
2019-12-02 문서 최초 작성

## 목표

1차 목표 : 10분 내외의 프로토타입 작성 ( 2019-12-02 ~ ) 

##### 1차 포함사항
 - character design (by CGM753)
 - background img design (by CGM753)
 - game system (by lkoiescg2031)
 - story(by lkoiescg2301, CGM753)
 - etc

## 개발 환경

lkoiescg2031  
OS: windows 10  
IDE: visualstudio 2019 16.3.10, unreal engine 4.23.1  
DOCS: markdown  

CGM
OS: windows 10  
TOOL: 3Dmax 2017, Zbrush 4R8, substance paint 2018, photoshop CC 2019, unreal engine 4.23.1  
DOCS: markdown  

TESTING  
OS :  
hardware spec :  

## 분석

### 10분 시연할 내용

TPS 장르로 동일한 몬스터를 잡으면 몬스터의 능력치가 올라가는 형식

장르: TPS, 로그라이크 

### 게임의 흐름

1. 플레어어와 커다란 하나의 몬스터가 한 공간에 생성됨 -> 배경, 스토리
2. 플레이어가 몬스터를 잡음 -> 몬스터 공격시스템, 플레이어의 조작시스템
4. 보상페이지가 열리고 플레이어는 보상을 받음 -> 보상시스템에 대해서 설정
5. 1 - 3을 반복함

### 배경
판타지, 엘프, 고블린, 숲

### 플레이어 시스템
 무기 2개 정도  
 이동 AWDS  
 가드 회피 무기교체  
 공격  
 HP, ~~스테미나,~~ 마나  
 
```
이동
플레이어가 움직일수 있는 방향 awds
```

```
가드 
공격을 막을 수 있음(데미지를 덜받음) + 후 딜레이 작음
타이밍이 일치하면 데미지또한 받지 않음
```

```
회피
공격을 막을 수 있음 (무적) + 후 딜레이가 큼
```

```
무기 교체
플레이어가 설정한 무기를 교체할 수 있음 + 딜레이 + 후 딜레이
 FOR 다른 속성에 대응하기 위함
```

```
공격 
무속성 공격 : 딜레이(피격 실패 시)
특정 속성 공격 : 마나소모(플레이어 능력치에 따른 소모량 결정) 
                + 후 딜레이(피격 실 패시)
```

```
마나
특정 속성 공격시 마다 소모 + 능력치에 따른 소모량 결정
마나에 회복속도가 존재 (느린 편)
```

```
HP
피격 될때마다 차감 (몬스터의 속성에 따른 차감)
0에 도달하면 사망
```

### 무기

총 {
 피격거리  
 피해량  
 속도  
 공격타입 {
  폭발  
  
 }  
}  
칼 {  
 피격거리  
 피해량  
 속도  
 공격타입 {  
  불  
  물  
  독  
  
 }  
}  

### 몬스터
한마리 치킨

### 기타 참조

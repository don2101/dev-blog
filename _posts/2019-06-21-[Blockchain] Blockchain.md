---
title: "Blockchain and P2P Network"
tags: ["Blockchain"]
---





# 블록체인

##### 2019. 06. 21 (Fri)

<br>

## 블록체인과 P2P 네트워크

<hr>

블록체인: 분산화 관리, 거래에 참여한 모두가 거래내역을 공유

<br>

### 1. 블록?

10분 마다의 거래내역을 모아놓은 단위

링크드리스트로 모든 블록이 연결되어 있다.

거래에 참여하는 모든 노드가 거래내역을 공유하며, 이러한 거래내역을 검증하고, 블록을 생성한다.

<br>

##### 실제로 모든 노드가 거래내역 검증에 참여?

그건 아니다. 실제로 거래내역은 거래 내역에 참여하는 어플리케이션을 받은 노드에만 저장되며, 이러한 노드들만 검증에 참여(full node)

<br>

##### 실제로 블록은 누구나 생성 가능하다

하나의 블록에 임의로 생성한 블록을 연결할 수 있다.

하지만, 이후에 연결되는 블록은 블록 길이가 가장 긴 흐름에 연결된다.

가장 긴 흐름이라는 것은 최대 6개 이상 블록이 연결된 것을 말한다

<br>

##### 왜 6개 인가?

악의를 가진 사용자가 블록 1~2개는 연결할 수 있다. 하지만 6개 이상의 블록을 임의로 연결하는 것은 현실적으로 불가능

<br>

<br>

#### 구조

##### header

이전 블록 해시값, time stamp, 해시문제 난이도, nonce(실제 찾아야 되는 값)

블록체인은 SHA-256 해시함수를 사용하여출력값을 생성하여 데이터 무결성을 보장

이전 노드 해시값, 타임 스탬프등 정보가 해시값으로 저장된다.

<br>

##### transaction

해당 블록에 들어간 거래 내역들

<br>

<br>

#### 해시값을 찾는다?

블록을 생성하기 위해서는 그 블록을 가리킬 해시값이 필요하다.

거래에 참여하는 노드들은 brute force 방식으로 nonce값을 찾아내어 해시값을 생성하고, 최초로 찾은 사람은 보상(약간의 코인, 거래 수수료)

빠르게 nonce값을 찾으려면 연산량이 빨라야 하며, 좋은 성능의 컴퓨터(gpu)가 필요

<br>

##### 왜 이렇게 불편한 방식을 사용?

그냥 코인에서 정한 **합의**이다.

코인마다 이 **합의의 방식**이 다르며, 비트코인은 이 방식을 사용한다.

<br>

<br>

### 2. 비트코인

탈중앙화된 장부

분산화: 참여자가 모든 사람의 거래내역을저장

P2P: 모든 노드가 서버이자 클라이언트이며, 모든 자료를 공유

한번 등록된 데이터는 수정과 삭제가 불가능하다

<br>

#### 비구조화 오버레이

<br>

<br>

<br>

## 블록체인과 디지털 서명

<hr>

부인방지: 모든 노드의 서명으로 거래 내역을 부인할 수 없다

공개키 기반 구조(비대칭키)로 서명을 대신한다.

개인키/공개키가 비대칭 키로 활용

블록체인은 송신자의 개인키로 서명(암호화)

- 암호화: 서명
- 복호화: 검증

<br>

<br>

<br>

## 블록체인 기초

<hr>

이더리움, 헤이퍼레저 패브릭 네트워크 구축

프론트엔드와 이더리움 간 연동

이더리움 스마트 컨트랙트 개발

하이퍼레저 패브릭 체인코드 개발



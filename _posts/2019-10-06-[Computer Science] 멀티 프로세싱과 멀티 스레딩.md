---
title: "멀티프로세싱과 멀티스레딩"
tags: ["Computer Science"]
---





### 멀티프로세싱과 멀티스레딩 vs 프로세스와 스레드

- 프로세스와 스레드는 소프트웨어 부분에서 다뤄지는 개념
- 멀티 프로세싱과 멀티스레딩은 하드웨어와 아키텍처 부분에서 다뤄지는 개념

<br>

## Multiprocessing

<hr>

- 컴퓨터에서 2개 이상의 CPU를 사용하는 것
- 사용하는 것을 넘어 2개 이상의 CPU가 메모리나 입력장치를 **공유**하는 구조
- 2개 이상의 CPU를 사용할 수 있는 시스템
- 2개 이상의 CPU를 사용하여 **병렬성**을 구현한 방식
- 메모리 사용 방식이나 데이터 공유에 따라 여러가지 구조가 존재

<br>

### 1. SMP(Symmetric Multiprocessing)

- 2개 이상의 CPU가 대칭을 이루는 구조
- 모든 CPU가 **메모리를 공유**하며 동등한 권리를 가진다.
  - 모두 **같은 물리적 메모리에 접근** 가능

<br>

### 2. ASMP(Asymmetric Multiprocessing)

- CPU마다 다른 권리를 갖는 구조
- 공유 메모리 구조를 가질 수 있지만, CPU마다 다른 처리를 맡게 될 수 있다.

<br>

<br>

## Multithreading

<hr>

- CPU에서 하나의 코어가 동시에 여러개의 프로세스나 스레드를 처리하는 것
- 프로세스나 스레드가 코어의 자원을 공유
- 멀티프로세싱은 **CPU가 메모리를 공유** vs 멀리스레딩은 **CPU와 코어 안의 작업이 메모리를 공유**
- 동시성을 OS level에서 극대화 하기 위한 개념

<br>

### 1. 특징

- 하드웨어에서 멀티스레딩이 가능하도록 설계해야 하며, 운영체제에서도 이를 지원해야 한다
  - 하드웨어 소프트웨어 둘다 구현 필요
- 하나의 CPU, 코어에서 다수의 프로세스나 스레드를 사용하기 위해 공통의 자원을 관리해야 한다.

<br>

### 2. Hyper-threading

- Intel에서 구현한 SMT(Simultaneous Multithreading)기술
- 물리적인 CPU의 코어가 1개에서 여러개로 보이도록 만드는 기술
  - **물리적인 코어**와 **논리적인 코어**를 구분해야 한다

<br>

<br>

## Multi-tasking

<hr>

- 동시에 하나 이상의 일을 처리하는 것
- **동시성**의 개념
- 작업을 나누어 처리하여 프로세서의 개수보다 동시에 많은 작업을 처리
- 작업 스케쥴링이 필요. 스케쥴링 방식에 따라 2가지로 분류

<br>

### 1. 선점형(Preemptive) 멀티 태스킹

- 우선순위에 의해 제어권을 선점하여 처리
- I/O Bound 작업을 효율적으로 처리할 수 있다
- **인터럽트**에 의해 제어권을 가져온다
- 프로세스가 중단될 수 있으므로, 자원에 대한 무결성을 위해 동기화 처리 필요

<br>

### 2. 비선점형(Non-Preemptive) 멀티 태스킹

- 진행중인 작업이 끝날 때 까지 기다리는 방식
  - 그럼 싱글태스킹이랑 다른게 뭐냐?
- 작업이 완료되지 않아도 다른 작업에게 제어권을 **자발적으로** 넘길 수 있다
- 제어권을 **프로세스가 조절**한다
- 작업이 유휴 상태이거나 특정 작업을 완료하면 제어권을 양보




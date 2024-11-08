# java-convenience-store-precourse

# 편의점 결제 시스템

## 프로젝트 개요
이 프로젝트는 편의점의 결제 시스템을 구현한 것입니다. 구매자의 할인 혜택과 재고 상황을 고려하여 최종 결제 금액을 계산하고 안내하는 기능을 제공합니다.

## 기능 목록
1. 상품 목록 및 재고 표시
2. 상품 구매 및 수량 입력
3. 프로모션 할인 적용 (N+1 행사)
4. 멤버십 할인 적용
5. 재고 관리
6. 영수증 출력
7. 추가 구매 옵션

## 기술 스택
- Java 21
- JUnit 5
- AssertJ

## 실행 방법
1. 프로젝트를 클론합니다.
2. `src/main/java/Application.java` 파일을 실행합니다.

## 주요 구현 사항

### 입력 처리
- 사용자로부터 구매할 상품과 수량을 입력받습니다.
- 입력 형식: `[상품명-수량],[상품명-수량]`
- 예: `[콜라-3],[사이다-2]`

### 할인 적용
- 프로모션 할인: N+1 행사 적용
- 멤버십 할인: 프로모션 미적용 금액의 30% 할인 (최대 8,000원)

### 재고 관리
- 구매 시 재고에서 차감
- 프로모션 재고와 일반 재고 구분 관리

### 영수증 출력
- 구매 상품 내역
- 증정 상품 내역
- 총구매액, 할인 금액, 최종 결제 금액 표시

### 예외 처리
- 잘못된 입력에 대한 예외 처리
- 재고 부족 시 예외 처리

## 프로그래밍 요구 사항
- indent depth는 2까지만 허용
- 3항 연산자 사용 금지
- else 예약어 사용 금지
- 메서드 길이 10라인 이하로 제한
- Java Enum 활용
- 단위 테스트 작성 (UI 로직 제외)

## 입출력 요구사항
- 상품 목록과 행사 목록은 파일 입출력으로 처리
- 사용자 입력은 Console 클래스의 readLine() 메서드 사용
- 현재 날짜와 시간은 DateTimes 클래스의 now() 메서드 사용

## 테스트
- JUnit 5와 AssertJ를 이용한 단위 테스트 구현

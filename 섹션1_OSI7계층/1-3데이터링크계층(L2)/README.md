# 데이터 링크 계층(L2,DataLink)

## 기본 개념

- 이진수로 구성된 데이터 이동

[ 목적지 ] ──► 1101

[ 출발지 ] ──► 10010

[ 유형 ] ──► 0011

[ 데이터 ] ──► 0110

[트레일러] ──► 10

## MAC 주소 활용

> MAC 주소는 개인 컴퓨터 또는 기계 주소를 말한다.

- MAC 주소는 0과1로된 데이터의 `목적지`와 `출발지`를 구분할 수 있다.
  - `목적지`엔 다른사람의 MAC 주소가 들어있다.
  - EX) 블루토스에서 00-0C-296C(랜카드ID) 같은 형태로.. 이건 `출발지` 주소다.

## 그런데 `목적지` MAC 주소는 어떻게 앎?

옆사람한테 물어본다.

어느 MAC 주소에 보내고 싶은데 그 주소를 잘 모르겠어 그러니까 너가 나 대신 물어봐줘,

그럼 얘는 또 다른 옆 사람에게 물어보고.. 이런식으로 쭉 가서 그 사람(MAC주소)을 찾게 되고 찾았으면 다시 반대 방향으로 돌아와서 `나에게` 알려준다.

### 옆사람이란?

스위치 포트 혹은 허브를 말한다.

참고로 허브는 동시에 데이터 전송시 충돌이 발생하기때문에 요즘은 `스위치가 대세`이다.

## 정리

1. 데이터 전송 경로:

- 출발지 (내 기기) → 스위치 → 라우터 → 인터넷 → 목적지 라우터

2. 주소 확인 과정:

- 기기가 스위치에게 목적지 주소를 문의
- 스위치는 라우터에게 경로를 문의
- 라우터는 인터넷을 통해 다른 라우터들과 통신하여 최적 경로 확인

3. 주소 체계:

- 출발지: 사용자의 기기 주소
- 목적지: 스위치의 네트워크 주소

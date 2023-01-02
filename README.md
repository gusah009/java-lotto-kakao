# java-lotto-kakao

## 기능 요구사항

- 로또 구입 금액을 입력하면 구입 금액에 해당하는 로또를 발급해야 한다.
- 로또 1장의 가격은 1000원이다.

## 기능 명세

- [x] 구입 금액을 입력받는 기능
- [x] 구입 금액에 따라 로또의 개수를 정하는 기능
- [x] 로또 개수에 따라 로또를 발급하는 기능
- [x] 구입한 로또 개수를 출력해주는 기능
- [x] 구입한 로또를 출력해주는 기능
- [x] 지난 주 당첨번호를 입력받는 기능
- [x] 보너스 볼을 입력받는 기능
- [x] 로또 1개의 등수를 정하는 기능
- [ ] 구입한 모든 로또의 등수를 출력해주는 기능
- [ ] 총 수익률을 계산하고 출력하는 기능

## 제약 사항

- 구매 금액
    - 구매 금액은 숫자여야 한다.
    - 구매 금액은 1000의 배수여야 한다.
    - 구매 금액은 [1000, Integer.MAX_VALUE] 범위 내여야 한다.
- 발급한 로또 번호
    - 발급한 로또 번호는 [1, 45] 범위 내여야 한다.
    - 발급한 로또 번호는 다 다른 숫자여야 한다.
    - 발급한 로또 번호는 6개이다.
    - 출력 시 발급한 로또 번호는 오름차순이어야 한다.
- 당첨 번호
    - 당첨 번호의 제약 사항은 발급한 로또 번호와 같다
- 보너스 번호
    - 보너스 번호의 범위는 발급한 로또 번호의 범위와 같다.
    - 보너스 번호는 당첨 번호와 다른 숫자여야 한다.
- 등수
    - 위치와 관계없이 숫자 3개가 일치할 경우 5,000원을 얻는다.
    - 위치와 관계없이 숫자 4개가 일치할 경우 50,000원을 얻는다.
    - 위치와 관계없이 숫자 5개가 일치하고, 보너스 번호가 일치하지 않을 경우 1,500,000원을 얻는다.
    - 위치와 관계없이 숫자 5개가 일치하고, 보너스 번호가 일치할 경우 30,000,000원을 얻는다.
    - 위치와 관계없이 숫자 6개가 일치할 경우 2,000,000,000원을 얻는다.
- 수익률 출력
    - 1보다 작을 경우: _"(기준이 1이기 때문에 결과적으로 손해라는 의미임)"_ 출력
    - 1일 경우: _"(기준이 1이기 때문에 결과적으로 구입금액과 수익이 일치한다는 의미임)"_ 출력
    - 1보다 클 경우: _"(기준이 1이기 때문에 결과적으로 이득이라는 의미임)"_ 출력

## 프로그래밍 요구사항

- 모든 로직에 단위 테스트를 구현한다. 단, UI(System.out, System.in) 로직은 제외
- indent(인덴트, 들여쓰기) depth를 2단계에서 1단계로 줄여라.
- depth의 경우 if문을 사용하는 경우 1단계의 depth가 증가한다. if문 안에 while문을 사용한다면 depth가 2단계가 된다.
- else를 사용하지 마라.
- 메소드의 크기가 최대 10라인을 넘지 않도록 구현한다.
- method가 한 가지 일만 하도록 최대한 작게 만들어라.
- **배열 대신 ArrayList를 사용한다.**
- java enum을 적용해 프로그래밍을 구현한다.
- **규칙 3: 모든 원시값과 문자열을 포장한다.**
- **규칙 5: 줄여쓰지 않는다(축약 금지).**
- **규칙 8: 일급 콜렉션을 쓴다.**
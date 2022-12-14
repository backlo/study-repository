# 스프링 클라우드 vs 쿠버네티스

## 스프링 클라우드

* 분산 환경에서의 공통적인 패턴을 빠르게 구축하도록 도와주는 도구를 제공
* 예를 들어 설정관리, 서비스 디스커버리, 서킷 브레이커, 라우팅 등. Neflix OSS 라이브러리 기반으로 만들어졌으며, `Java` 개발자를 위해 만들어짐
* 강점
  * 스프링 플랫폼과 스프링 부트의 빠른 어플리케이션 생성 능력에 의해 제공되는 **통합 프로그래밍 모델**은 개발자에게 훌륭한 마이크로서비스 개발 경험을 제공
  * 실행시간의 주요한 것들을 다룰 수 있는 **다양한 선택지의 라이브러리들**이 있음
  * 다른 스프링 클라우드 라이브러리들은 다른 라이브러리완 쉽게 통합
* 약점
  * 자바에 한정적
  * **개발자및 자바 어플리케이션에 너무 많은 책임**이 주어짐
  * 스프링 클라우드는 MSA 세계에 있어서 **일부분의 기능만을 제공**



## 쿠버네티스

* 그리고 **모든 언어에 대해 보편적인 방식으로 분산 컴퓨팅 문제들에 대한 답을 제시**
* 쿠버네티스는 설정 관리, 서비스 디스커버리, 로드 밸런싱, 추적, 매트릭스, 싱글톤, 스케쥴 잡을 위한 서비스를 플랫폼 레벨에서, 어플리케이션 스택의 외부에서 제공
* 어플리케이션은 클라이언트 사이드의 로직을 위한 어떠한 라이브러리와 agent가 필요하지 않음
* 그리고 어떠한 언어에서도 적용될 수 있음



## 특징 정리

| 스프링                                           | 쿠버네티스                                      |
| ------------------------------------------------ | ----------------------------------------------- |
| JVM 환경 강점                                    | JVM 관리 강점                                   |
| 어플리케이션 패키징                              | 배포, 스케쥴링                                  |
| Hystrix 스레드풀 활용 어플리케이션 내부 벌크헤딩 | 자원, 프로세스, 네임스페이스 격리 활용 벌크헤딩 |
| 상태 엔드 포인트 제공                            | 상태 확인, 트래픽 라우팅                        |
| 설정 외부화, 업데이트                            | 설정 배포                                       |
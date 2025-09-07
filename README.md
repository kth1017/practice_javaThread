# 멀티스레드 기본
주로 실무에선
executorSerive 스레드 풀 관리 / BlockingQueue 버퍼 관리 / 코드 구현 Callable+Future 

# Lock
- 생산자 소비자 문제를 통한 이해
- JAVA 1.0 기본 모니터락 synchronized : 기본 내장 BLOCKED, WAITING state 구분
- JAVA 1.5 LockSupport, ReentrantLock : 모니터락 대신 자체 구현 lock, WAITING만을 사용, 개별 Condition(스레드 대기 공간) 구현 가능
- JAVA 1.5 CAS, concurrentLock : 스핀락 방식의 CAS 락 구현

  * race condition 증가로 JVM의 무거운 락 확장시 OS 레벨의 뮤텍스, 세마포어 등 호출

# CompletableFuture
- JAVA 1.8 도입
- thread.get()으로 인한 블로킹 개선
- Future 합성 및 예외처리 편의성 증가
- JS의 Promise 패턴과 유사한 비동기 프로그래밍 도구

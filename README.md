# Upbit BB JS Bridge Probe

Bug bounty 분석용 PoC 호스팅. 본인 (HOHK1017 / hohk) 계정만 사용 검증.

## URL
- 메인: https://hohk0923.github.io/upbit-poc/
- Echo: https://hohk0923.github.io/upbit-poc/echo.html

## 사용
1. 본인 S23에서 `https://hohk0923.github.io/upbit-poc/` 직접 방문 → 외부 Chrome에서 열리는지 확인
2. 페이지 안의 deep link 클릭 → mobile app이 어떻게 처리하는지 확인
3. 만약 mobile app WebView로 열리면 → JS bridge `window.Upbit` 노출 여부 확인 → bridge method probe

## 정직성
- 본 PoC는 **본인 device**에서만 사용
- **타인 자산/계정 접근 시도 안 함**
- 캡처되는 정보는 본인 token 또는 환경 정보만 (자체 device)
- BB scope `*.upbit.com` + Android app `com.dunamu.exchange` 안

## 주의
- Cert pinning 우회 안 함
- Frida injection 안 함 (objection patchapk 시도했으나 native crash로 차단됨)
- 정상 deep link mediator 동작 검증만

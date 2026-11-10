# Agent 365 관련 API 검증 결과

Agent 365로 에이전트를 조회하고 제어할 때 쓸 수 있는 API를 **DIA 데모 테넌트**에서 실제로 호출해, 각 기능이 가능한지 불가능한지 확인한 결과입니다.

**보고서 보기: https://akimcse.github.io/agent365-api-verification/**

## 무엇이 들어 있나

- 항목별 검증 결과: 사용한 API, 확인한 결과, 판정(가능 / 불가능 / 확인 못 함)
- 쓰기 API 요약
- 아직 확인하지 못한 항목과 다음에 시도할 방법
- 실제 호출 기록: 요청(메서드, 주소, 인증, 본문)과 응답

Agent 365 전용 API만 다루지 않고, Agent 365가 기반으로 삼는 제품의 API도 함께 다룹니다.
Microsoft Graph(Entra Agent ID, 보안, ID Governance), Defender 고급 헌팅, Purview 감사, Power Platform, Intune, Agent 365 관측성 수집 등입니다.

## 읽을 때 알아둘 점

- 모든 결과는 DIA 데모 테넌트(Microsoft 365 E7 라이선스 보유) 기준입니다. 데이터나 정책이 없어서 나온 결과(예: 해당 이벤트 0건)는 다른 테넌트에서 다를 수 있습니다.
- 쓰기 API는 되돌릴 수 있는 것만 호출했고, 만든 테스트 객체는 삭제하거나 원복했습니다.
- beta 경로의 API가 많아 이후 동작이 바뀔 수 있습니다.
- 앱 시크릿과 토큰은 보고서에서 가렸습니다.
- 검증 기간: 2026-11-06 ~ 11-10

## 구성

| 파일 | 설명 |
|---|---|
| `index.html` | 보고서 본문(한 파일로 된 정적 HTML, 외부 리소스 없음) |
| `.github/workflows/pages.yml` | `main`에 푸시하면 GitHub Pages로 배포 |

## 업데이트 방법

1. `index.html`을 새 버전으로 교체합니다.
2. `main`에 푸시합니다.
3. Actions의 **Deploy to GitHub Pages**가 끝나면 사이트가 갱신됩니다. Actions 탭에서 수동 실행(`workflow_dispatch`)도 가능합니다.

<div align="center">

# 티팟 라우터 — 코딩 에이전트용 LLM API 게이트웨이

**키 하나. 프로토콜 둘. 쓴 만큼만 — 잔액은 절대 만료되지 않습니다.**

클로드 코드(Claude Code) · Codex CLI · OpenAI SDK 도구를 위한 호스티드 게이트웨이(AI API 중계): 환경변수 두 개만 바꾸면 모든 AI 코딩 도구가 하나의 엔드포인트, 하나의 잔액, 요청별 비용 장부로 연결됩니다.

[시작하기](https://teapotrouter.com/ko/register) · [가격 — 공개, 머신 리더블 JSON](https://teapotrouter.com/api/pricing) · [문서](https://teapotrouter.com/ko/docs)

</div>

---

## 코딩 에이전트에 왜 게이트웨이인가?

Claude Code와 OpenAI SDK 도구를 함께 돌리면 이런 경험이 익숙할 겁니다: 도구마다 엔드포인트와 키가 따로 필요하고, 청구서는 매월 블랙박스가 됩니다.

게이트웨이는 이 배관을 정리합니다:

|  | 직접 연결(벤더별) | 게이트웨이 경유 |
| --- | --- | --- |
| 엔드포인트 & 키 | 벤더마다 하나씩 | **키 하나, 프로토콜 둘** |
| 청구 | 대시보드 N개, 월 합계만 | 잔액 하나, **요청별 장부** |
| 비용 가시성 | "\$84 나왔다" | "그 세션은 \$6.20 — 78%는 다시 전송된 컨텍스트" |
| 약관 | 벤더별 정책 | 여기는: **잔액 무기한**, 잔여 금액 기준 환불 |

## 설정: 환경변수 두 개

```bash
# Claude Code (Anthropic 프로토콜)
export ANTHROPIC_BASE_URL="https://api.teapotrouter.com"
export ANTHROPIC_AUTH_TOKEN="sk-****"

# OpenAI SDK / Codex CLI — 같은 키, /v1 엔드포인트
# base_url = https://api.teapotrouter.com/v1
```

등록 → 첫 요청 → 문제 해결까지 단계별 가이드: [teapotrouter.com/ko/docs](https://teapotrouter.com/ko/docs)

## 사이트에서 확인할 수 있는 것

- [무료 비용 계산기 (로그인 불필요, 실시간 요금)](https://teapotrouter.com/ko/claude-code-cost-calculator) — 구독 vs 종량 과금 손익분기점 확인
- **공개 가격** — 모든 모델의 기준 요금과 실제 지불 금액. 로그인 없는 JSON 엔드포인트([`/api/pricing`](https://teapotrouter.com/api/pricing))로 스크립트 비교도 가능
- **모델별 가격 페이지** — 예: [claude-opus-5-5](https://teapotrouter.com/ko/pricing/claude-opus-5-5)
- **Claude Code 가격 가이드** — 구독 vs 종량 과금 vs 게이트웨이, 실제 비용 계산 포함: [문서](https://teapotrouter.com/ko/docs/claude-code-pricing)
- **문제 해결 가이드** — 연결 실패 · 401 · 쿼터(quota) 에러를 원인별 해결책과 매칭: [문서](https://teapotrouter.com/ko/docs/claude-code-troubleshooting)

## 어떤 게이트웨이든 물어야 할 두 가지 (여기도 예외 아님)

- **모델은 어디서 조달하나?** 공식·공인 API 채널에서 사용량 기반으로 결제하며 조달합니다. 계정 공유, 구독 재판매는 하지 않습니다.
- **무엇이 기록되나?** 결제 메타데이터만(모델, 토큰, 비용, 지연시간) — 요청별 장부가 가능한 이유입니다. "제로 로그" 연출은 하지 않습니다. 대화 내용은 다루지 않습니다.

## 솔직한 한계

1인 개발, 최근 출시, 마케팅 예산 없음 — 가격 엔드포인트는 항상 살아있는 모델 목록을 보여주니, 이 README를 믿기보다 직접 확인하세요. 멀티 업스트림 페일오버가 내장되어 있어도 게이트웨이는 하나의 의존성입니다. 대체 경로를 남겨 두세요.

문의: support@teapotrouter.com

---

<div align="center">

이름은 HTTP 상태 코드 418 "I'm a teapot"에서 왔습니다 🫖 — [풀 스토리](https://teapotrouter.com/ko/418)

**[Teapot Router](https://teapotrouter.com/ko)** — Claude Code와 GPT를 위한 stability-first AI 게이트웨이

</div>

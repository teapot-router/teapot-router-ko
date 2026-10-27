# Teapot Router (티팟 라우터)

**개발자용 AI 모델 API 게이트웨이** — 하나의 키로 Claude Code와 OpenAI SDK를 모두 하나의 엔드포인트로.

공식 사이트: <https://teapotrouter.com/ko>

## - **듀얼 프로토콜**: Anthropic Messages(Claude Code 호환)와 OpenAI Chat Completions(`/v1`)를 동일 키로 지원
- **사용량 기반 과금·가격 전면 공개**: 무료 JSON 가격 API(`/api/pricing`) 제공
- **요청별 비용 기록**: 모델·토큰·금액을 매번 기록
- **조직 키 발급·감사 로그**
- **멀티 업스트림 자동 페일오버**

## Claude Code 빠른 시작

```bash
export ANTHROPIC_BASE_URL=https://api.teapotrouter.com
export ANTHROPIC_AUTH_TOKEN=sk-xxxx
claude
```

## OpenAI SDK / Codex CLI 빠른 시작

```bash
export OPENAI_BASE_URL=https://api.teapotrouter.com/v1
export OPENAI_API_KEY=sk-xxxx
```

## 가격

사용량 기반 과금(선불, $1부터 충전).
가격: <https://teapotrouter.com/ko> / JSON: <https://teapotrouter.com/api/pricing>

## 이 프로젝트에 대해

- 개인 개발 프로젝트입니다
- 이름은 HTTP 상태 코드 418 "I'm a teapot"에서 유래했습니다 🫖
- 문의: support@teapotrouter.com
# triz-agents

[English README](README.md)

**알트슐러의 TRIZ 전체 프레임워크를 Claude Code 스킬로 구현.**

TRIZ 방법론을 AI 에이전트 스킬로 구현한 최초의 오픈소스 프로젝트. 외부 의존성 없이 `.claude/` 폴더만 복사하면 바로 사용 가능.

## TRIZ란?

TRIZ(발명 문제 해결 이론)는 겐리흐 알트슐러가 창안한 체계적 혁신 방법론이다. 40만 건 이상의 특허를 분석하여 발명적 해결책에는 반복되는 패턴이 있다는 것을 발견했다. TRIZ는 불가능해 보이는 문제에서 이 패턴을 찾아 해결하는 도구를 제공한다.

> "깨달음을 100년 기다릴 수도 있고, 이 원리들로 15분 만에 풀 수도 있다." — 알트슐러

## 제공 도구

### 문제 분석

| 명령어 | 도구 | 기능 | 근거 |
|--------|------|------|------|
| `/triz "문제"` | **전체 워크플로우** | IFR → 모순 → 원리 → 자원 → 해결안 | ARIZ-85C |
| `/triz:ifr` | **이상적 최종 결과** | 비용·해악·복잡성 제로인 완벽한 해결 정의 | *그리고 갑자기 발명가가 나타났다* |
| `/triz:contradiction` | **모순 분석** | 기술적·물리적 모순 도출 | *정밀 과학으로서의 창의성* |

### 해결안 생성

| 명령어 | 도구 | 기능 | 근거 |
|--------|------|------|------|
| `/triz:matrix` | **모순 행렬** | 39개 파라미터 매핑 → 추천 원리 도출 | 39×39 Matrix |
| `/triz:40p` | **40가지 발명 원리** | 모순 해결을 위한 원리 적용 | 40 Principles |
| `/triz:sufield` | **물질-장 분석** | 물질-장 상호작용 모델링 및 개선 | Su-Field 모델 |
| `/triz:resources` | **자원 분석** | 시스템과 환경의 숨겨진 자원 탐색 | ARIZ 4단계 |

### 시스템 설계

| 명령어 | 도구 | 기능 | 근거 |
|--------|------|------|------|
| `/triz:trimming` | **트리밍** | 구성요소 제거로 시스템 단순화 | TRIZ+ / VE |
| `/triz:evolution` | **진화 패턴** | 8가지 패턴으로 차세대 시스템 예측 | *진화의 패턴* |
| `/triz:ariz` | **ARIZ** | 알고리즘 기반 전체 문제 해결 프로세스 | ARIZ-85C |

## 설치

### 방법 1: 프로젝트에 복사

```bash
# 저장소 클론
git clone https://github.com/ironyjk/triz-agents.git

# .claude/ 폴더를 프로젝트에 복사
cp -r triz-agents/.claude/commands/triz* your-project/.claude/commands/
cp -r triz-agents/.claude/skills/triz your-project/.claude/skills/
```

### 방법 2: 직접 실행

```bash
cd triz-agents
claude   # 이 디렉토리에서 Claude Code 실행
```

그리고 명령어 실행:
```
/triz "처리량을 늘려야 하는데 장비를 추가하면 유지보수 비용이 늘어난다"
```

## 빠른 시작

### 물리적 모순 해결

```
/triz:contradiction "파이프가 설치 시에는 단단해야 하고 운용 시에는 유연해야 한다"
```

출력: 기술적·물리적 모순 + 분리 전략.

### 시스템 단순화

```
/triz:trimming "이 장비는 15개 부품으로 구성되어 있는데 원가가 너무 높다"
```

출력: 기능 가치 기준 부품 순위, 트리밍 후보, 재설계안.

### 전체 혁신 분석

```
/triz "처리량을 늘려야 하는데 장비를 추가하면 유지보수 비용이 늘어난다"
```

출력: ARIZ 기반 전체 분석 — IFR, 모순, 자원, 원리, 해결 컨셉.

### 기술 진화 예측

```
/triz:evolution "3D 프린팅 기술"
```

출력: S-커브 상 현재 위치, 적용 가능한 진화 패턴, 차세대 기술 예측.

## 전체 워크플로우 구조

```mermaid
graph LR
    P["문제"] --> IFR["1. IFR<br/>이상적 최종 결과"]
    IFR --> C["2. 모순 분석<br/>TC + PC"]
    C --> R["3. 자원 분석<br/>숨겨진 자원"]
    R --> PR["4. 원리 적용<br/>40가지 원리"]
    PR --> S["5. 해결안<br/>컨셉 도출"]
    
    style IFR fill:#6c5ce7,color:#fff
    style C fill:#d63031,color:#fff
    style R fill:#00b894,color:#fff
    style PR fill:#e17055,color:#fff
    style S fill:#0984e3,color:#fff
```

전체 워크플로우는 **5단계 순차 파이프라인**으로 진행된다:

1. **IFR 단계** — 이상적 상태 정의: 비용·해악·복잡성 없이 기능만 달성
2. **모순 단계** — IFR 도달을 막는 것 식별: 기술적 모순(IF...THEN...BUT)과 물리적 모순(A이면서 not-A)
3. **자원 단계** — 활용 가능한 모든 자원 조사: 물질, 장(field), 공간, 시간, 정보, 기능
4. **원리 단계** — 40가지 발명 원리 중 가장 적합한 원리 선택 및 적용
5. **해결안 단계** — 발명 수준과 실현 가능성으로 순위 매긴 구체적 해결 컨셉 생성

각 단계는 이전 단계 결과를 기반으로 진행되며, 최종 보고서에서 실행 가능한 해결안으로 종합된다.

## 출력 형식

모든 도구는 **Mermaid** (기본) 또는 **ASCII** 형식으로 출력한다:

```
/triz:contradiction "속도 vs 정확도" --format ascii
```

Mermaid 다이어그램은 GitHub, VS Code 등 대부분의 마크다운 뷰어에서 기본 렌더링된다.

## 이론 배경

[docs/altshuller-background.md](docs/altshuller-background.md)에서 알트슐러의 생애, TRIZ 발전사, 주요 저서, 전 세계 확산 과정을 상세히 다룬다.

## 예제

- [제조 문제](examples/manufacturing-problem.md) — 단단하면서 유연한 파이프 (모순 + 40원리)
- [소프트웨어 아키텍처](examples/software-architecture.md) — 캐시인데 실시간인 웹앱 (IFR + 행렬)
- [원가 절감](examples/cost-reduction.md) — 품질 유지하면서 원가 절감 (트리밍 + 자원)
- [차세대 설계](examples/next-gen-design.md) — 전기차 배터리 진화 예측 (진화 패턴 + S-커브)

## 로드맵

### v1.0 (현재)
- [x] 문제 분석 도구 3종 (전체 워크플로우, IFR, 모순 분석)
- [x] 해결안 생성 도구 4종 (행렬, 40원리, 물질-장, 자원)
- [x] 시스템 설계 도구 3종 (트리밍, 진화 패턴, ARIZ)
- [x] Mermaid + ASCII 출력
- [x] ARIZ 기반 전체 워크플로우 파이프라인

### v2.0 (예정)
- [ ] **효과 데이터베이스** — 8,000건 이상의 물리·화학·기하 효과로 해결안 생성
- [ ] **특허 분석** — 특허 DB에서 모순과 원리 자동 추출
- [ ] **기능 분석** — 기능 순위 포함 구성요소 상호작용 모델링
- [ ] **9-화면** — 멀티스크린 (시스템/상위/하위 × 과거/현재/미래)

### v3.0 (예정)
- [ ] **MCP 서버** — TRIZ 도구를 MCP 리소스로 노출하여 프로젝트 간 공유
- [ ] **대화형 모드** — 각 단계마다 사용자 입력을 받는 가이드 분석
- [ ] **TRIZ-TOC 통합** — 제약 식별(TOC)과 발명적 문제 해결(TRIZ) 결합
- [ ] **사례 라이브러리** — 해결된 문제와 적용 원리 검색 데이터베이스

## /think 와 함께 사용 (30개 도구)

TRIZ는 다른 프레임워크와 함께 쓸 때 더 강력합니다. [strategy-frameworks](https://github.com/ironyjk/strategy-frameworks)를 설치하면 `/think` 메타 에이전트를 사용할 수 있습니다 — 문제를 말하면 30개 도구 중 최적의 조합을 자동 선택합니다.

```bash
# 30개 도구 한번에 설치 (TOC + TRIZ + 9개 전략 프레임워크 + /think)
curl -fsSL https://raw.githubusercontent.com/ironyjk/strategy-frameworks/master/install.sh | bash
```

## 관련 프로젝트

- [strategy-frameworks](https://github.com/ironyjk/strategy-frameworks) — Wardley, OODA, Porter, Blue Ocean, Design Thinking, Drucker, BSC, First Principles + `/think`
- [toc-agents](https://github.com/ironyjk/toc-agents) — 제약이론(TOC) 11개 도구

## 저자

**최희철** — DY산업개발 대표이사
[Claude Code](https://claude.ai/claude-code) (Anthropic Claude Opus 4.6)와 공동 제작

## 라이선스

[MIT](LICENSE)

## 감사의 말

- **겐리흐 알트슐러** (1926-1998) — TRIZ 창안자
- 수십 년간 연구와 적용을 이어온 전 세계 TRIZ 커뮤니티
- [toc-agents](https://github.com/ironyjk/toc-agents)에서 영감을 받아 제작

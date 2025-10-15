---
name: pp
description: "Smart prompt recommender - AI-driven adaptive prompt recommendations with command validation and fallback mechanisms"
category: optimization
complexity: moderate
mcp-servers: ["context7", "sequential"]
version: "3.1.0"
---

# /pp - Smart Prompt Recommender

**🎯 AI가 사용자 프롬프트를 분석하여 최적의 슈퍼클로드/플러그인 명령어로 변환** - `/pp "[사용자 프롬프트]" SuperClaude와 Claude Code Plugins(claude-code-settings, superpowers 등)를 이용해 가장 효과적인 프롬프트를 만들어줘.`

## 🚀 빠른 시작

```bash
# 기본 사용법
/pp "React 컴포넌트 개발해줘"

# 복잡한 분석 요청
/pp "앱 성능 최적화 방법 찾아줘"

# 비즈니스 전략 수립
/pp "신사업 기획서 작성해줘"
```

## ⚡ 핵심 특징

- **🧠 지능적 분석**: 프롬프트 의도와 복잡성 자동 분석
- **🔄 실시간 검증**: 모든 명령어 동시 스캔 및 유효성 확인
- **⚡ 최적 매칭**: 슈퍼클로드, 플러그인, MCP 서버 중 최적 도구 선택
- **🛡️ 자동 대체**: 없는 명령어 → 가장 유사한 대체 명령어로 자동 교체
- **📊 명확한 설명**: 각 추천의 강점과 사용 시점 구체적 명시
- **⭐ 추천 이유**: 왜 이 명령어가 효과적인지 구체적 근거 제시

## 🚨 중요: 파일 수정 제한

**⚠️ PP 명령어는 오직 프롬프트 변환 기능만 수행하며, 어떠한 파일도 직접 수정하지 않습니다.**

### 🛡️ 안전 보장 원칙
- **✅ 읽기 전용**: 코드 분석, 검토, 조사만 수행
- **❌ 파일 수정**: 어떤 파일도 직접 생성, 수정, 삭제하지 않음
- **🔍 명령어 추천**: 최적의 명령어만 제안하고 실행은 사용자가 직접 결정
- **⚡ 안전장치**: 우발적 파일 변경 방지를 위한多重 보호 시스템

### 🎯 PP의 역할
PP는 **"지능적인 안내자"**이지 **"실행자"**가 아닙니다:

## 🔍 실시간 명령어 검증 시스템

PP 명령어 실행 시 자동으로 현재 사용 가능한 모든 명령어를 스캔합니다:

### 1. SuperClaude 명령어 (SC Commands)
```bash
# /Users/hjshin/.claude/commands/sc/ 디렉토리 스캔
sc:analyze, sc:brainstorm, sc:build, sc:business-panel, sc:cleanup,
sc:design, sc:document, sc:estimate, sc:explain, sc:git, sc:implement,
sc:improve, sc:index, sc:load, sc:reflect, sc:save, sc:select-tool,
sc:spawn, sc:spec-panel, sc:task, sc:test, sc:troubleshoot, sc:workflow
```

### 2. 플러그인 명령어 (Plugin Commands)
```bash
# Claude Code Plugins Marketplace
claude-code-settings:analyze, claude-code-settings:implement, claude-code-settings:tasks,
claude-code-settings:kiro:design, claude-code-settings:kiro:spec, claude-code-settings:kiro:task,
claude-code-settings:kiro:vibe, claude-code-settings:gh:fix-issue, claude-code-settings:gh:review-pr,
commit-commands:commit, commit-commands:commit-push-pr, commit-commands:clean_gone,
feature-dev:feature-dev, pr-review-toolkit:review-pr, agent-sdk-dev:new-sdk-app
```

### 3. superpowers 명령어
```bash
# superpowers Commands
superpowers:brainstorm, superpowers:execute-plan, superpowers:write-plan,
superpowers:collision-zone-thinking, superpowers:inversion-exercise,
superpowers:meta-pattern-recognition, superpowers:scale-game,
superpowers:simplification-cascades, superpowers:when-stuck
```

### 4. 그 외의 Claude Code Plugins
항상 사용할 수 있는 명령어인지 확인하고 추천해야 함.

## 🎯 명령어 추천 알고리즘

### 1단계: 프롬프트 분석
- **의도 파악**: 사용자 목적 분석 (개발, 분석, 기획, 디버깅 등)
- **복잡성 평가**: 단순 작업 vs 복합적 분석 필요
- **도메인 식별**: 기술, 비즈니스, 디자인 등 분야 확인

### 2단계: 명령어 매칭
- **실시간 스캔**: 현재 사용 가능한 모든 명령어 목록 확인
- **유사도 계산**: 프롬프트-명령어 간 매칭 점수 계산
- **적합성 평가**: 사용자 요구사항과 명령어 기능 비교

### 3단계: 최적 추천
- **상위 3개**: 가장 적합한 명령어 3개 추천
- **강점 분석**: 각 명령어의 장점과 사용 시점 명시
- **대체 안내**: 없는 명령어 → 유사한 대체 명령어 제안

## 🚀 사용 예시

### 기술 개발 요청
```bash
# 사용자 입력
/pp "React 타입스크립트 컴포넌트 만들어줘"

# PP 추천 결과
🎯 **1위 추천**: /claude-code-settings:kiro:vibe
   📍 이유: 빠른 개발 지원, 컴포넌트 아키텍처 자동 생성
   🌟 강점: 즉시 실행 가능한 코드 제공

🎯 **2위 추천**: /ui-engineer
   📍 이유: React/TypeScript 전문 UI 개발
   🌟 강점: 접근성과 성능 최적화된 컴포넌트

🎯 **3위 추천**: /sc:implement
   📍 이유: 구조화된 개발 프로세스
   🌟 강점: 단계별 구현 및 품질 보증
```

### 분석 요청
```bash
# 사용자 입력
/pp "코드 품질 분석해줘"

# PP 추천 결과
🎯 **1위 추천**: /sc:analyze
   📍 이유: 다중 도메인 분석 전문 명령어
   🌟 강점: 품질/보안/성능 종합 분석

🎯 **2위 추천**: /code-reviewer
   📍 이유: 코드 품질 및 베스트 프랙티스 검토
   🌟 강점: 실행 가능한 개선 제안

🎯 **3위 추천**: /quality-engineer
   📍 이유: 테스트 전략 및 엣지 케이스 분석
   🌟 강점: 체계적 품질 보증 방법론
```

## ⚙️ 실행 방식

### 자동 검증 프로세스
1. **명령어 스캔**: 사용 가능한 모든 명령어 실시간 확인
2. **유효성 검증**: 각 명령어의 동작 여부 확인
3. **매핑 업데이트**: 최신 명령어 목록으로 추천 시스템 갱신

### 안전 장치
- **읽기 전용**: 코드 분석 및 검토만 수행
- **실행 보류**: 추천만 제공, 실제 실행은 사용자 결정
- **대체 제공**: 없는 명령어 → 가장 유사한 대체 명령어 자동 매핑

## 📊 추천 기준

### 매칭 점수 요소
- **의도 일치도** (40%): 사용자 목적과 명령어 기능 일치 정도
- **복잡성 적합도** (25%): 요청 복잡성과 명령어 처리 능력
- **도메인 전문성** (20%): 특정 분야 전문화 수준
- **사용 용이성** (15%): 직관성과 학습 곡선

### 최종 순위 결정
- 총점 순위 상위 3개 명령어 추천
- 동점일 경우 최신 업데이트 명령어 우선
- 플러그인 의존성 확인하여 사용 가능한 명령어만 추천
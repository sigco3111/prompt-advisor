# Prompt Advisor 커스텀 슬래시 커맨드 사용 가이드

> **작성일**: 2025-10-15 (v2.4.0 업데이트)
> **명령어**: `/prompt-advisor`, `/pp` (AI 기반 스마트 프롬프트 추천기)
> **목적**: AI가 사용자 프롬프트를 분석하여 최적의 변형을 동적으로 추천
> **새로운 기능**: 명령어 검증 시스템, 자동 대체 메커니즘, 오류 방지, 신뢰성 강화 (v2.4.0)

---

## 🔧 **설치 방법**

### **1. 파일 복사**
```bash
# 프로젝트 디렉토리에서 다음 명령어 실행
cp prompt-advisor.md ~/.claude/commands/
cp pp.md ~/.claude/commands/
```

### **2. 권한 설정**
```bash
# 실행 권한 부여 (필요시)
chmod 755 ~/.claude/commands/prompt-advisor.md
chmod 755 ~/.claude/commands/pp.md
```

### **3. 설치 확인**
```bash
# Claude Code에서 명령어 사용 가능 여부 확인
/prompt-advisor --help
/pp "test prompt"
```

### **설치 경로**
- **Linux/macOS**: `~/.claude/commands/`
- **Windows**: `%USERPROFILE%\.claude\commands\`

**중요**: Claude Code가 명령어를 인식하려면 반드시 `.claude/commands` 디렉토리에 파일이 위치해야 합니다.

---

## 🎯 **개요**

이 프로젝트는 두 가지 커스텀 슬래시 커맨드를 제공합니다:

### **1. `/prompt-advisor` - 전문가급 프롬프트 전략**
복잡한 프로젝트를 체계적으로 진행할 수 있도록 최적의 프롬프트 전략과 스킬 시퀀스를 추천하는 지능형 커맨드입니다.

### **2. `/pp` - 스마트 프롬프트 추천기 v2.4.0**
AI가 사용자 프롬프트의 의도와 복잡성을 분석하여 최적의 변형을 동적으로 추천하는 지능형 커맨드입니다. **명령어 검증 시스템**으로 "Unknown slash command" 오류를 완전히 방지하고, **자동 대체 메커니즘**으로 항상 유효한 명령어만 추천합니다.

---

## 📋 **명령어별 사용법**

### **1. `/prompt-advisor` - 상세 전략 추천**
```bash
/prompt-advisor [작업/설명] [--strategy 전략] [--plugins 모드] [--skills 모드] [--output 출력형식]
```

**매개변수 설명:**
- **[작업/설명]**: 수행할 작업에 대한 간단한 설명
- **--strategy**: 사용할 전략 (brainstorm|design|implement|analyze)
- **--plugins**: 플러그인 사용 모드 (auto|all|list|none)
- **--skills**: 스킬 사용 모드 (auto|all|list|minimal)
- **--output**: 출력 형식 (brief|detailed|template)

### **2. `/pp` - 스마트 프롬프트 추천기**
```bash
/pp "[변환하고 싶은 프롬프트]"             # AI가 최적의 개수와 순위로 추천
/pp "웹사이트 디자인 해줘" --context=current-project    # 맥락 인식
/pp "로그인 기능 구현해줘" --interactive              # 상호작용 모드
/pp --save "자주 쓰는 프롬프트"                       # 즐겨찾기 저장
/pp --load                                             # 즐겨찾기 목록
/pp "api 문서 작성" --alias=api-doc                    # 별칭 사용
```

**v2.4.0 핵심 기능:**
- 🧠 **지능적 분석**: 프롬프트의 의도와 복잡성을 자동으로 분석
- 🔄 **유연한 추천**: 고정된 4개 대신 상황에 맞는 최적의 개수 제공 (2-5개)
- ⭐ **별점 평가**: 각 추천의 효과성을 별점으로 표시
- 📊 **특징 설명**: 각 추천의 강점과 사용 시점 명시
- 💡 **추천 이유**: 왜 이 프롬프트가 효과적인지 구체적 설명
- ✅ **즉시 실행 가능**: 복사-붙여넣기 바로 가능한 명령어
- 🛡️ **명령어 검증 시스템**: 모든 추천 명령어의 실제 존재 여부를 동적으로 확인 (v2.4.0 신규)
- 🔄 **자동 대체 메커니즘**: 없는 명령어는 가장 유사한 대체 명령어로 자동 교체 (v2.4.0 신규)
- 🚨 **오류 방지**: "Unknown slash command" 오류를 완전히 방지 (v2.4.0 신규)
- 📋 **다중 레벨 폴백**: 4단계에 걸친 안전한 명령어 대체 시스템 (v2.4.0 신규)
- 📊 **모니터링 시스템**: 지속적인 개선을 위한 사용 패턴 추적 (v2.4.0 신규)

---

## 🚀 **사용 예시**

### **명령어별 비교 예시**

#### **프롬프트 변환 (v2.3 AI 기반 동적 추천)**
```bash
# /pp 사용 (단일 프롬프트 → AI가 최적의 개수와 순위로 추천)
/pp "웹사이트 디자인 해줘"

🎯 **"웹사이트 디자인 해줘" - 4가지 맞춤 접근법**

**1. 🎨 사용자 경험 중심 디자인** ⭐⭐⭐⭐⭐
**특징**: 직관적이고 매력적인 사용자 인터페이스
**추천 이유**: 성공적인 웹사이트의 핵심은 사용자 경험
```
/sc:design 사용자 중심의 반응형 인터페이스와 고객 여정 맵 기반의 직관적 디자인 --ux-first --mobile-optimized
```

**2. 🏗️ 기술 구현 중심 접근** ⭐⭐⭐⭐
**특징**: 확장 가능하고 안정적인 기술 아키텍처
**추천 이유**: 장기적인 관리와 확장성을 위한 기반 마련
```
/sc:architecture 성능 최적화된 컴포넌트 기반 웹사이트와 확장 가능한 API 구조 설계 --performance-focused --scalable
```

**3. 💼 비즈니스 목표 중심 접근** ⭐⭐⭐⭐
**특징**: 전환율과 ROI를 극대화하는 비즈니스 지향 디자인
**추천 이유**: 웹사이트의 궁극적 목표는 비즈니스 성과
```
/sc:design 전환율 최적화와 브랜드 일관성을 고려한 비즈니스 목표 지향 디자인 --conversion-focused --roi-driven
```

**4. ⚡ 빠른 프로토타이핑 접근** ⭐⭐⭐
**특징**: 시장 검증을 위한 빠른 최소 기능 제품
**추천 이유**: 아이디어 검증과 시장 테스트에 가장 효과적
```
/sc:template 검증된 템플릿 활용과 빠른 목업 제작으로 시장 검증용 최소 기능 웹사이트 구축 --rapid-prototyping --market-validation
```

# /prompt-advisor 사용 (상세 전략)
/prompt-advisor "implement user authentication system" --strategy implement
# → Phase 1: /sc:brainstorm "auth requirements and security considerations"
# → Phase 2: /sc:design authentication-system --focus security
# → Phase 3: /sc:task auth-implementation --plugins sequential,context7
# → Phase 4: /sc:implement auth-middleware + /sc:implement session-management
# → Phase 5: /sc:analyze auth-security --focus security
```

#### **프롬프트 변형 예시 (v2.3 AI 분석)**
```bash
# /pp 사용 (AI가 프롬프트 복잡성을 분석하여 최적의 접근법 추천)
/pp "인증 버그 수정해줘"

🎯 **"인증 버그 수정해줘" - 3가지 해결 방법**

**1. 🔍 체계적 분석 접근** ⭐⭐⭐⭐⭐
**특징**: 근본 원인 분석과 재발 방지
**추천 이유**: 버그 수정의 핵심은 근본적 해결과 재발 방지
```
/sc:analyze 인증-흐름 --security-audit
/sc:identify 근본-원인 --systematic-investigation
/sc:design 포괄적-수정 --prevent-regression
/sc:test 모든-인증-시나리오 --complete-coverage
/sc:document 수정-및-예방 --knowledge-transfer
```

**2. ⚡ 빠른 핫픽스 접근** ⭐⭐⭐⭐
**특징**: 즉각적인 문제 해결과 서비스 안정성
**추천 이유**: 긴급 상황에서 가장 빠른 복구 필요
```
/sc:identify 빠른-수정 --minimal-impact
/sc:implement 패치 --rollback-ready
/sc:test 핵심-경로 --essential-functions
/sc:deploy 핫픽스 --production-safe
/sc:monitor 안정성 --post-deployment
```

**3. 🛡️ 보안 중심 접근** ⭐⭐⭐
**특징**: 보안 취약점 점검과 강화
**추천 이유**: 인증 관련 문제는 보안 위협과 직결
```
/sc:security-audit 인증 --vulnerability-scan
/sc:design 보안-강화 --defense-in-depth
/sc:implement 보안-수정 --zero-trust-principle
/sc:penetration-testing --security-validation
/sc:implement 모니터링 --threat-detection
```

# /prompt-advisor 사용 (체계적 분석)
/prompt-advisor "fix authentication bug" --strategy analyze --output detailed
# → 상세한 원인 분석, 다양한 해결책 비교, 위험 평가 포함
```

#### **다양한 프롬프트 변형 예시 (v2.3 AI 추천)**
```bash
# /pp 사용 (AI가 프롬프트를 분석하여 최적의 접근법 3가지 추천)
/pp "pp 명령어 개선 사항을 제안해줘"

🎯 **"pp 명령어 개선 사항을 제안해줘." - 3가지 최적 접근법**

**1. 🎨 사용자 경험 중심 개선** ⭐⭐⭐⭐⭐
**특징**: 직관적이고 개인화된 추천 시스템
**추천 이유**: 사용자 만족도를 극대화하는 가장 효과적인 접근법
```
/sc:design 개인화된 추천 알고리즘으로 사용자 패턴 학습 및 최적화된 프롬프트 제안 --user-centric --adaptive-learning
```

**2. 🏗️ 기술 아키텍처 확장** ⭐⭐⭐⭐
**특징**: 확장 가능하고 안정적인 시스템 설계
**추천 이유**: 장기적인 관점에서 지속 가능한 발전 기반 제공
```
/sc:architecture 동적 프롬프트 생성 엔진과 커뮤니티 기반 템플릿 공유 플랫폼 구축 --scalable --ecosystem-driven
```

**3. ⚡ 빠른 실행 중심 개선** ⭐⭐⭐
**특징**: 즉각적인 효과와 빠른 구현
**추천 이유**: 단기간에 눈에 띄는 개선 효과 제공
```
/sc:improve 맥락 인식과 템플릿 다양성을 통한 즉각적인 사용성 개선 --quick-wins --context-aware
```
```

### **상황별 추천 (v2.4 AI 기반 신뢰성 강화)**

#### **1. 동적 프롬프트 변형**
```bash
/pp "AI 블로그 글 작성해줘"                 # AI가 3-4가지 글쓰기 접근법 추천
/pp "간단한 계산기 만들어줘"                  # AI가 2-3가지 개발 방식 추천
/pp "데이터베이스 설계해줘"                     # AI가 3-4가지 데이터베이스 설계 추천
/pp "pp 명령어 개선 방안 제안해줘"             # AI가 3가지 개선 접근법 추천
```

#### **2. AI 분석 카테고리별 예시**
```bash
# 🎯 목표 지향 프롬프트: 명확한 결과물 요구
/pp "웹사이트 디자인 해줘"                    # 4가지 맞춤 접근법 (⭐⭐⭐⭐⭐ ~ ⭐⭐⭐)

# 🔍 탐구형 프롬프트: 학습, 조사 필요
/pp "머신러닝 배우는 방법 알려줘"             # 3가지 학습 경로 추천

# ⚡ 실행형 프롬프트: 빠른 액션 필요
/pp "버그 빨리 수정해줘"                      # 2-3가지 빠른 해결책

# 🎭 창의형 프롬프트: 아이디어 생성
/pp "신제품 아이디어 제안해줘"                # 3-4가지 창의적 접근법
```

#### **2. 복잡한 프로젝트 계획**
```bash
/prompt-advisor "이커머스 플랫폼 구축" --strategy design --output detailed
/prompt-advisor "마이크로서비스 이전" --plugins all
/prompt-advisor "ML 파이프라인 구현" --strategy implement --skills auto
```

#### **3. 전략적 분석 필요**
```bash
/prompt-advisor "시스템 성능 최적화" --strategy analyze
/prompt-advisor "기술 스택 선택" --output template
```

---

## 🎨 **실전 시나리오**

### **시나리오 1: TF-IDF 시맨틱 검색 구현**

#### **/pp로 빠르게 시작**
```bash
/pp "FAQ 시스템용 TF-IDF 시맨틱 검색 구현"
# → /sc:design tfidf-semantic-search --focus performance --plugins context7
# → /sc:implement korean-text-processor
# → /sc:implement tfidf-calculator
# → /sc:implement semantic-search-engine
# → /sc:test semantic-search-functionality
```

#### **/prompt-advisor로 상세 계획**
```bash
/prompt-advisor "FAQ 시스템용 TF-IDF 시맨틱 검색 구현" --strategy implement --plugins auto
# → Phase 1: Discovery + Phase 2: Architecture + Phase 3: Planning
# → Phase 4: Core Implementation + Phase 5: Integration & Testing
# (각 단계별 상세 가이드 포함)
```

### **시나리오 2: iOS 앱 개발**

#### **/pp로 빠르게 시작**
```bash
/pp "구독 기능이 있는 iOS 명상 앱 개발"
# → /sc:design ios-meditation-app --focus ux --plugins magic,context7
# → /sc:implement meditation-session-ui --plugins magic
# → /sc:implement subscription-system --plugins sequential
# → /sc:test app-functionality
```

#### **/prompt-advisor로 상세 계획**
```bash
/prompt-advisor "구독 기능이 있는 iOS 명상 앱 개발" --strategy design --plugins auto
# → Requirements Discovery → System Design → Architecture Planning
# → Feature Implementation → Quality Assurance
# (각 단계별 상세 가이드 포함)
```

### **시나리오 3: 데이터 파이프라인 구축**

#### **/pp로 빠르게 시작**
```bash
/pp "실시간 분석용 ETL 파이프라인 구축"
# → /sc:design etl-pipeline --focus scalability --plugins sequential
# → /sc:implement data-extraction-service
# → /sc:implement transformation-engine
# → /sc:implement loading-mechanism
# → /sc:analyze pipeline-performance
```

#### **/prompt-advisor로 상세 계획**
```bash
/prompt-advisor "실시간 분석용 ETL 파이프라인 구축" --strategy implement --plugins all
# → Architecture Design → Implementation Planning → Parallel Development
# → Integration & Optimization (고급 플러그인 활용)
```

---

## 🛠️ **플러그인 통합 가이드 (v2.0 NEW!)**

### **사용 가능한 고급 플러그인**

#### 🎯 **claude-code-plugins**
- **GitHub 통합**: PR 생성, 이슈 관리, 코드 리뷰
- **개발 자동화**: 빌드 프로세스, 테스트 파이프라인
- **프로젝트 관리**: 작업 추적, 마일스톤 관리

#### ⚙️ **claude-code-settings**
- **구성 관리**: 설정 최적화, 환경 설정
- **커스텀 명령어**: 명령어 생성, 워크플로우 자동화
- **개인화**: 선호도 관리, 프로필 최적화

#### 🚀 **superpowers**
- **고급 워크플로우**: 복잡한 다단계 프로세스
- **스킬 통합**: 특화된 전문 지식 접근
- **성능 최적화**: 속도와 효율성 향상

#### 🧠 **criticalthink**
- **분석 강화**: 깊이 있는 비판적 사고 프레임워크
- **문제 해결**: 체계적 이슈 해결
- **의사결정 지원**: 증거 기반 추천

#### 🏢 **business-panel**
- **전문가 분석**: 9명의 비즈니스 사상가 패널
- **전략적 통찰**: 경쟁 분석, 시장 동향
- **위험 평가**: 체계적 비즈니스 리스크 관리

### **도메인별 플러그인 매트릭스**

| 도메인 | 핵심 플러그인 | 분석 도구 | 테스트 스위트 | 비즈니스 도구 |
|--------|--------------|-----------|---------------|----------------|
| **프론트엔드** | magic, context7 | sequential | playwright | claude-code-settings |
| **백엔드** | sequential, context7 | serena | sequential | superpowers |
| **데이터 과학** | sequential, context7 | serena | - | criticalthink |
| **DevOps** | sequential, serena | context7 | - | claude-code-plugins |
| **비즈니스** | context7, sequential | claude-code-settings | - | business-panel |
| **AI/ML** | sequential, context7 | superpowers, criticalthink | - | claude-code-plugins |

### **플러그인 최적화 팁**

#### **초보자**
```bash
/pp "simple task" --level beginner
# 기본 플러그인: magic, context7, sequential
# 보조 도구: claude-code-settings
```

#### **중급 사용자**
```bash
/pp "moderate complexity" --level intermediate
# 핵심 플러그인: sequential, context7
# 보조 도구: magic, serena, superpowers
```

#### **고급 사용자**
```bash
/pp "complex enterprise project" --level advanced
# 핵심 플러그인: sequential, context7, serena
# 전문 도구: claude-code-plugins, criticalthink
```

---

## 🔧 **명령어 선택 가이드**

### **언제 어떤 명령어를 사용해야 할까?**

| 상황 | 추천 명령어 | 이유 |
|------|-------------|------|
| **빠른 아이디어 실행** | `/pp` | 복잡한 옵션 없이 즉시 시작 가능 |
| **간단한 작업 시작** | `/pp` | 5개 이내의 명령어로 충분 |
| **복잡한 프로젝트 계획** | `/prompt-advisor` | 상세한 단계별 계획 필요 |
| **전략적 분석 필요** | `/prompt-advisor` | 다양한 관점에서 분석 제공 |
| **팀 프로젝트** | `/prompt-advisor` | 체계적인 문서화와 계획 |
| **학습 및 연구** | `/prompt-advisor` | 상세한 설명과 배경 제공 |

### **복잡도별 추천**

| 복잡도 | 추천 명령어 | 특징 |
|--------|-------------|------|
| **단순** (1-2단계) | `/pp` | 빠르고 직접적인 실행 |
| **중간** (3-5단계) | `/pp` 또는 `/prompt-advisor` | 필요에 따라 선택 |
| **복잡** (6+단계) | `/prompt-advisor` | 체계적인 계획 필요 |
| **전문가** (아키텍처) | `/prompt-advisor` | 상세 분석과 전략 필수 |

### **플러그인 최적화 가이드**

#### **작업 타입별 추천 플러그인**
| 작업 타입 | 추천 플러그인 | 명령어 사용법 |
|-----------|-------------|--------------|
| **UI/UX 개발** | magic, context7 | `/pp "design dashboard"` → 자동 플러그인 추천 |
| **복잡한 로직** | sequential, context7 | `/pp "implement algorithm"` → 최적 플러그인 조합 |
| **데이터 처리** | sequential, serena | `/pp "analyze data"` → 데이터 처리 최적화 |
| **테스트 자동화** | playwright, sequential | `/pp "test website"` → 테스트 전략 제공 |

#### **플러그인 활용 팁**
- **UI 개발**: `magic` 플러그인으로 빠른 컴포넌트 생성
- **복잡한 알고리즘**: `sequential` 플러그인으로 단계적 해결
- **데이터 분석**: `context7` 플러그인으로 베스트 프랙티스 적용
- **자동화**: `playwright` 플러그인으로 테스트 자동화

### **스킬 시퀀스 패턴**

#### **기본 워크플로우**
- **개발**: 탐색 → 설계 → 구현 → 테스트
- **분석**: 이해 → 설계 → 구현 → 검증
- **문제 해결**: 분석 → 설계 → 구현 → 확인

#### **고급 패턴**
- **병렬 실행**: 여러 구성요소 동시 개발
- **반복적 개선**: 설계 → 구현 → 분석 → 재설계
- **통합적 접근**: 다양한 관점에서 복합적 해결

---

## 📊 **효과성 측정**

### **성과 지표**
- **명령어 정확도**: 추천된 명령어가 작업 요구사항과 일치하는 정도
- **실행 효율성**: 제안된 워크플로우의 실제 실행 속도
- **플러그인 활용**: 적절한 플러그인 선택과 조합의 효과
- **시간 절약**: 수동 계획 대비 자동화된 절감 시간

### **사용 패턴 분석**
- **빈도 분석**: 어떤 작업 타입이 가장 많은가?
- **성공률**: 추천된 명령어의 실제 실행 성공률
- **선호도**: `/pp` vs `/prompt-advisor` 사용 비율
- **피드백**: 사용자 만족도와 개선 제안

---

## 🎯 **모범 사례**

### **성공적인 사용 패턴**

#### **1. 명령어 선택 전략**
```bash
# 빠른 시작 - /pp 사용
/pp "create simple landing page"
/pp "setup basic authentication"
/pp "build contact form"

# 상세 계획 - /prompt-advisor 사용
/prompt-advisor "develop complete e-commerce platform" --strategy design
/prompt-advisor "migrate legacy system to cloud" --output detailed
```

#### **2. 상황별 최적 활용**
```bash
# 프로젝트 시작: /pp로 빠른 아이디어 구체화
/pp "plan mobile app structure"

# 중간 계획: /prompt-advisor로 상세 전략 수립
/prompt-advisor "design app architecture" --strategy design

# 문제 해결: 작업 크기에 따라 선택
/pp "fix small UI bug"
/prompt-advisor "solve complex performance issue" --strategy analyze
```

### **효과적인 사용 팁**

#### **1. 구체적인 작업 설명**
```bash
# ❌ 나쁜 예시
/pp "build something"
/prompt-advisor "make app"

# ✅ 좋은 예시
/pp "build responsive portfolio website with contact form"
/prompt-advisor "develop real-time chat app with encryption"
```

#### **2. 적절한 명령어 선택**
```bash
# 단순 작업: /pp
/pp "add login button"
/pp "create simple API endpoint"

# 복잡 작업: /prompt-advisor
/prompt-advisor "implement complete authentication system"
/prompt-advisor "design microservices architecture"
```

#### **3. 컨텍스트 포함**
```bash
# ❌ 나쁜 예시
/pp "implement authentication"
/prompt-advisor "optimize database"

# ✅ 좋은 예시
/pp "implement JWT authentication for React Node.js app"
/prompt-advisor "optimize PostgreSQL queries for analytics dashboard"
```

## 🛡️ **v2.4.0 신규: 명령어 검증 및 오류 방지 시스템**

### **"Unknown slash command" 오류 완전 해결**

#### **문제 원인 및 해결**
```bash
# 과거 문제 (v2.3.1 이전)
/pp "코드 개선해줘"
→ /sc:enhance 코드 개선 제안
→ 실행: "Unknown slash command: sc:enhance" ❌

# v2.4.0 해결
/pp "코드 개선해줘"
→ 🔄 자동 검증: sc:enhance 없음
→ 📋 대체 명령어: sc:improve
→ 📝 안내: "sc:enhance 대신 sc:improve를 사용합니다"
→ ✅ 정상 출력: /sc:improve 코드 개선 및 최적화
```

### **명령어 검증 프로세스**
1. **사전 검증**: 추천된 모든 명령어의 실제 존재 여부 확인
2. **자동 대체**: 없는 명령어는 가장 유사한 기능의 명령어로 교체
3. **사용자 알림**: 명령어 변경 시 명확한 이유와 대안 제시
4. **다중 폴백**: 4단계에 걸친 안전한 명령어 대체 시스템

### **대체 명령어 매핑 테이블**
| 원본 명령어 | 대체 명령어 | 변경 사유 | 기능 설명 |
|------------|------------|-----------|-----------|
| `sc:enhance` | `sc:improve` | 개선 기능 통합 | 코드 품질 향상 |
| `sc:optimize` | `sc:improve` | 최적화 기능 포함 | 성능 개선 |
| `sc:refactor` | `sc:improve` | 리팩토링 기능 포함 | 코드 구조 개선 |
| `sc:create` | `sc:implement` | 생성 기능 동일 | 새로운 기능 추가 |
| `sc:build` | `sc:implement` | 구축 기능 동일 | 시스템 구현 |

### **사용자 경험 개선**
```
🔄 **명령어 자동 교체 안내**

원본: /sc:enhance (존재하지 않는 명령어)
→ 대체: /sc:improve (코드 개선 및 최적화)

이유: 'enhance' 기능은 'improve' 명령어에 통합되었습니다.
영향: 동일한 결과를 얻을 수 있으며, 더 안정적인 동작을 보장합니다.
```

---

## 🔍 **트러블슈팅**

### **일반적인 문제 해결**

#### **1. 추천이 너무 복잡할 때**
```bash
# /pp로 더 간단한 접근
/pp "build simple feature"

# /prompt-advisor로 간소화된 옵션
/prompt-advisor "task" --strategy implement --output brief --plugins minimal
```

#### **2. 특정 도구가 필요할 때**
```bash
# 플러그인 직접 지정
/pp "task requiring specific tools"
# → 필요한 플러그인 자동 추천

/prompt-advisor "task" --plugins sequential,context7
```

#### **3. 시간 제약이 있을 때**
```bash
# /pp로 빠른 실행
/pp "urgent feature needed now"

# /prompt-advisor로 빠른 전략
/prompt-advisor "urgent task" --strategy implement --output template
```

#### **4. 명령어가 작동하지 않을 때**
```bash
# 설치 확인
ls ~/.claude/commands/

# 파일 권한 확인
chmod 755 ~/.claude/commands/pp.md
chmod 755 ~/.claude/commands/prompt-advisor.md

# Claude Code 재시작
```

---

## 🚀 **결론**

두 개의 커스텀 슬래시 커맨드를 통해 슈퍼클로드의 강력한 기능을 최적으로 활용할 수 있습니다.

### **핵심 장점**

#### **`/pp` v2.4.0 - AI 기반 스마트 프롬프트 추천기**
- ✅ **지능적 분석**: 프롬프트의 의도와 복잡성을 자동으로 분석
- ✅ **유연한 추천**: 고정된 4개 대신 상황에 맞는 최적의 개수 제공 (2-5개)
- ✅ **별점 평가**: 각 추천의 효과성을 별점(⭐)으로 표시
- ✅ **특징 설명**: 각 추천의 강점과 사용 시점 명시
- ✅ **추천 이유**: 왜 이 프롬프트가 효과적인지 구체적 설명
- ✅ **즉시 실행 가능**: 복사-붙여넣기 바로 실행
- ✅ **명령어 검증 시스템**: 모든 추천 명령어의 실제 존재 여부를 동적으로 확인 (v2.4.0 신규)
- ✅ **자동 대체 메커니즘**: 없는 명령어는 가장 유사한 대체 명령어로 자동 교체 (v2.4.0 신규)
- ✅ **오류 방지**: "Unknown slash command" 오류를 완전히 방지 (v2.4.0 신규)
- ✅ **신뢰성 강화**: 항상 유효한 명령어만 추천 (v2.4.0 신규)

#### **`/prompt-advisor` - 전문가급 전략**
- ✅ **상세 분석**: 복잡한 작업에 대한 체계적 접근
- ✅ **전략적 계획**: 단계별 실행 계획과 가이드
- ✅ **유연성**: 다양한 옵션과 맞춤형 설정
- ✅ **품질 보증**: 포괄적인 검토와 최적화

### **성공적인 사용을 위한 팁**

#### **1. 명령어 선택 기준**
- **빠른 시작**: `/pp`로 즉시 실행
- **복잡한 계획**: `/prompt-advisor`로 상세 전략
- **학습 목적**: `/prompt-advisor`로 상세한 이해

#### **2. 효과적인 사용법**
1. **구체적인 작업 설명**: 명확하고 상세한 작업 정의
2. **적절한 명령어 선택**: 작업 복잡도에 맞는 도구 선택
3. **단계적 실행**: 추천된 워크플로우 순서대로 실행
4. **결과 피드백**: 실행 결과를 바탕으로 다음 단계 계획

### **v2.4.0 새로운 기능 시작하기**
```bash
# 설치
cp pp.md ~/.claude/commands/
cp prompt-advisor.md ~/.claude/commands/

# v2.4.0 빠른 테스트 (명령어 검증 및 오류 방지)
/pp "코드 개선해줘"                # 🔄 자동 검증: sc:enhance → sc:improve
/pp "웹사이트 디자인 해줘"          # AI가 4가지 맞춤 접근법 추천 (별점 포함, 유효한 명령어만)
/pp "인증 버그 수정해줘"             # AI가 3가지 해결 방식 추천 (오류 없는 명령어)
/pp "pp 명령어 개선 방안 제안해줘"     # AI가 3가지 개선 접근법 추천 (신뢰성 강화)

# 기본 테스트
/prompt-advisor "웹 애플리케이션 계획" --strategy brainstorm
```

### **성공적인 사용을 위한 핵심 팁**

#### **1. v2.4.0 신뢰성 강화 기능 활용**
- **명령어 검증 시스템**: 모든 추천 명령어의 실제 존재 여부를 동적으로 확인
- **자동 대체 메커니즘**: 없는 명령어는 가장 유사한 대체 명령어로 자동 교체
- **오류 방지**: "Unknown slash command" 오류를 완전히 방지
- **사용자 안내**: 명령어 변경 시 명확한 이유와 대안 제시
- **신뢰성 강화**: 항상 유효한 명령어만 추천하여 안정적인 사용 경험 제공
- **모니터링 시스템**: 지속적인 개선을 위한 사용 패턴 추적 (v2.4.0 신규)

#### **2. 명령어 선택 기준**
- **빠른 변환**: `/pp`로 AI 기반 동적 추천
- **상세 계획**: `/prompt-advisor`로 체계적 전략 수립

#### **3. AI 분석 카테고리 이해**
- **🎯 목표 지향**: 명확한 결과물 요구 시 최적화된 접근법
- **🔍 탐구형**: 학습, 조사 필요 시 체계적 분석 제공
- **⚡ 실행형**: 빠른 액션 필요 시 간결한 해결책 제시
- **🎭 창의형**: 아이디어 생성 시 다양한 관점 제공
- **🛠️ 기술형**: 구체적 기술 구현 시 전문적 접근법
- **💼 비즈니스형**: 전략, ROI, 목표 달성 중심 접근

이제 두 명령어를 활용하여 어떤 아이디어든 효과적으로 실행할 수 있습니다! 🚀✨
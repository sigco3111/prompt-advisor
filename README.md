# Prompt Advisor 커스텀 슬래시 커맨드 사용 가이드

> **작성일**: 2025-10-14
> **명령어**: `/prompt-advisor`
> **목적**: 슈퍼클로드 스킬과 플러그인을 최적으로 활용하는 지능형 프롬프트 전략 추천

---

## 🔧 **설치 방법**

### **1. 파일 복사**
```bash
# 프로젝트 디렉토리에서 다음 명령어 실행
cp prompt-advisor.md ~/.claude/commands/
```

### **2. 권한 설정**
```bash
# 실행 권한 부여 (필요시)
chmod 755 ~/.claude/commands/prompt-advisor.md
```

### **3. 설치 확인**
```bash
# Claude Code에서 명령어 사용 가능 여부 확인
/prompt-advisor --help
```

### **설치 경로**
- **Linux/macOS**: `~/.claude/commands/`
- **Windows**: `%USERPROFILE%\.claude\commands\`

**중요**: Claude Code가 명령어를 인식하려면 반드시 `.claude/commands` 디렉토리에 파일이 위치해야 합니다.

---

## 🎯 **개요**

`/prompt-advisor`는 사용자의 작업을 분석하여 가장 효과적인 슈퍼클로드 스킬 시퀀스와 플러그인 조합을 추천하는 지능형 커맨드입니다. 복잡한 프로젝트를 체계적으로 진행할 수 있도록 최적의 프롬프트 전략을 제공합니다.

---

## 📋 **기본 문법**

```bash
/prompt-advisor [작업/설명] [--strategy 전략] [--plugins 모드] [--skills 모드] [--output 출력형식]
```

### **매개변수 설명**

- **[작업/설명]**: 수행할 작업에 대한 간단한 설명
- **--strategy**: 사용할 전략 (brainstorm|design|implement|analyze)
- **--plugins**: 플러그인 사용 모드 (auto|all|list|none)
- **--skills**: 스킬 사용 모드 (auto|all|list|minimal)
- **--output**: 출력 형식 (brief|detailed|template)

---

## 🚀 **사용 예시**

### **1. 기본 사용법**
```bash
# 간단한 작업에 대한 프롬프트 추천
/prompt-advisor "implement user authentication system"

# 결과 추천:
# 1. /brainstorm "auth requirements and security considerations"
# 2. /design authentication-system --focus security
# 3. /task auth-implementation --plugins sequential,context7
# 4. /implement auth-middleware
# 5. /analyze auth-security --focus security
```

### **2. 전략 지정 사용**
```bash
# 브레인스토밍 중심 접근
/prompt-advisor "create mobile app for fitness tracking" --strategy brainstorm

# 설계 중심 접근
/prompt-advisor "design microservices architecture" --strategy design

# 구현 중심 접근
/prompt-advisor "build API server with Node.js" --strategy implement

# 분석 중심 접근
/prompt-advisor "optimize database performance" --strategy analyze
```

### **3. 플러그인 최적화**
```bash
# 자동 플러그인 선택
/prompt-advisor "develop React dashboard" --plugins auto

# 모든 플러그인 사용
/prompt-advisor "complex system integration" --plugins all

# 플러그인 목록만 보기
/prompt-advisor "web development project" --plugins list --output brief
```

### **4. 출력 형식 제어**
```bash
# 간결한 추천
/prompt-advisor "setup testing framework" --output brief

# 상세한 분석 포함
/prompt-advisor "migrate to cloud architecture" --output detailed

# 실행 가능한 템플릿
/prompt-advisor "implement CI/CD pipeline" --output template
```

---

## 🎨 **실전 시나리오**

### **시나리오 1: TF-IDF 시맨틱 검색 구현**
```bash
/prompt-advisor "implement TF-IDF semantic search for FAQ system" --strategy implement --plugins auto

# 추천 결과:
# Phase 1: Discovery
# /brainstorm "current CSV limitations and TF-IDF approach" --depth normal

# Phase 2: Architecture Design
# /design tfidf-semantic-search --focus performance --plugins context7

# Phase 3: Implementation Planning
# /task tfidf-implementation --plugins sequential,context7 --skills auto

# Phase 4: Core Implementation
# /implement korean-text-processor
# /implement tfidf-calculator
# /implement semantic-search-engine

# Phase 5: Integration & Testing
# /implement csv-service-integration
# /test semantic-search-functionality
# /analyze search-performance --focus optimization
```

### **시나리오 2: iOS 앱 개발**
```bash
/prompt-advisor "build iOS meditation app with subscription" --strategy design --plugins auto

# 추천 결과:
# Phase 1: Requirements Discovery
# /brainstorm "meditation app features and monetization" --strategy systematic

# Phase 2: System Design
# /design ios-meditation-app --focus ux --plugins magic,context7

# Phase 3: Architecture Planning
# /task ios-implementation-plan --plugins sequential,context7

# Phase 4: Feature Implementation
# /implement meditation-session-ui --plugins magic
# /implement subscription-system --plugins sequential
# /implement progress-tracking

# Phase 5: Quality Assurance
# /analyze app-performance --focus mobile-optimization
# /test subscription-flow
```

### **시나리오 3: 데이터 파이프라인 구축**
```bash
/prompt-advisor "build ETL pipeline for real-time analytics" --strategy implement --plugins all

# 추천 결과:
# Phase 1: Architecture Design
# /design etl-pipeline --focus scalability --plugins sequential,context7

# Phase 2: Implementation Planning
# /task etl-implementation --plugins sequential,context7,serena

# Phase 3: Parallel Development
# /implement data-extraction-service --parallel-execution
# /implement transformation-engine --parallel-execution
# /implement loading-mechanism --parallel-execution

# Phase 4: Integration & Optimization
# /implement pipeline-orchestration
# /analyze pipeline-performance --focus throughput
```

---

## 🔧 **고급 기능**

### **1. 작업 복잡도별 추천**

| 복잡도 | 추천 스킬 | 플러그인 전략 | 예상 시간 |
|--------|------------|---------------|-----------|
| **단순** (1-2단계) | 직접 실행 | 최소 플러그인 | 30분-1시간 |
| **중간** (3-5단계) | 작업 분해 | 문맥 기반 플러그인 | 2-4시간 |
| **복잡** (6+단계) | 멀티 스킬 조정 | 전략적 플러그인 사용 | 1일-3일 |
| **전문가** (아키텍처) | 전체 스킬 오케스트레이션 | 고급 통합 | 3일-1주 |

### **2. 플러그인 최적화 패턴**

#### **성능 최적화**
```bash
# 복잡한 알고리즘 구현
/prompt-advisor "implement machine learning pipeline" --plugins sequential,context7

# 결과: Sequential MCP로 복잡한 로직 처리, Context7 MCP로 프레임워크 가이드
```

#### **품질 보증**
```bash
# 포괄적인 테스트 전략
/prompt-advisor "comprehensive testing strategy" --plugins sequential,context7 --output detailed

# 결과: 체계적인 분석과 모범 사례 적용
```

#### **개발 가속화**
```bash
# UI 컴포넌트 대량 생성
/prompt-advisor "build React component library" --plugins magic,morphllm

# 결과: Magic MCP로 UI 컴포넌트, Morphllm MCP로 대량 변환
```

### **3. 스킬 체이닝 전략**

#### **순차적 의존성**
```markdown
탐색 → 설계 → 계획 → 구현 → 분석
```

#### **병렬 실행**
```markdown
- 다른 포커스를 가진 여러 /implement 작업
- 여러 시스템 컴포넌트에 대한 병렬 /design
- 여러 도메인에 대한 동시 /analyze
```

#### **반복적 개선**
```markdown
설계 → 구현 → 분석 → 재설계 → 재구현
```

---

## 📊 **성과 측정**

### **효과성 지표**
- **프롬프트 정확도**: 추천된 프롬프트가 작업 요구사항과 얼마나 잘 일치하는가
- **스킬 활용도**: 스킬-작업 매핑의 효율성
- **플러그인 최적화**: 리소스 사용량과 성능 향상
- **완료 시간**: 전체 프로젝트 가속화 정도

### **지속적인 학습**
```swift
// 사용 패턴 기반 추천 개선
class PromptOptimizer {
    func analyzeRecommendationEffectiveness(
        originalTask: Task,
        recommendedPrompts: [Prompt],
        actualOutcome: Outcome
    ) -> OptimizationInsights
}
```

---

## 🎯 **모범 사례**

### **성공적인 사용 패턴**

#### **1. 프로젝트 시작 단계**
```bash
# 프로젝트 초기 계획 수립
/prompt-advisor "plan new e-commerce platform" --strategy brainstorm --output detailed
```

#### **2. 기술적 결정 시점**
```bash
# 아키텍처 의사결정
/prompt-advisor "choose between microservices vs monolith" --strategy analyze
```

#### **3. 성능 최적화 필요 시**
```bash
# 시스템 성능 개선
/prompt-advisor "optimize API response time" --strategy analyze --plugins sequential
```

#### **4. 복잡한 기능 구현**
```bash
# 복잡한 비즈니스 로직
/prompt-advisor "implement real-time collaboration features" --strategy implement --plugins all
```

### **피해야 할 실수**

#### **1. 불충분한 작업 설명**
```bash
# ❌ 나쁜 예시
/prompt-advisor "build something"

# ✅ 좋은 예시
/prompt-advisor "build real-time chat application with message encryption"
```

#### **2. 잘못된 전략 선택**
```bash
# ❌ 나쁜 예시 (단순 작업에 과도한 분석)
/prompt-advisor "add login button" --strategy analyze --output detailed

# ✅ 좋은 예시
/prompt-advisor "add login button" --strategy implement --output brief
```

#### **3. 컨텍스트 무시**
```bash
# ❌ 나쁜 예시 (프로젝트 컨텍스트 고려 안함)
/prompt-advisor "implement authentication"

# ✅ 좋은 예시 (구체적인 컨텍스트 포함)
/prompt-advisor "implement JWT authentication for React Node.js app"
```

---

## 🔍 **트러블슈팅**

### **일반적인 문제들**

#### **1. 추천이 너무 복잡한 경우**
```bash
# 더 간단한 추천 요청
/prompt-advisor "simple task" --strategy implement --plugins minimal --output brief
```

#### **2. 특정 스킬이나 플러그인이 필요한 경우**
```bash
# 구체적인 리소스 지정
/prompt-advisor "task" --plugins sequential,context7 --skills auto
```

#### **3. 시간 제약이 있는 경우**
```bash
# 빠른 전략 요청
/prompt-advisor "urgent task" --strategy implement --output template --plugins minimal
```

---

## 🚀 **결론**

`/prompt-advisor`는 슈퍼클로드의 강력한 기능을 최적으로 활용할 수 있도록 돕는 지능형 조력자입니다.

### **핵심 장점**
- **지능형 분석**: 작업을 자동으로 분석하여 최적의 접근 방식 추천
- **자원 최적화**: 사용 가능한 스킬과 플러그인을 효율적으로 조합
- **시간 절약**: 최적의 프롬프트 시퀀스로 개발 시간 단축
- **품질 향상**: 체계적인 접근으로 더 나은 결과물 도출

### **성공적인 사용을 위한 팁**
1. **구체적인 작업 설명**: 명확하고 상세한 작업 정의
2. **적절한 전략 선택**: 작업 특성에 맞는 전략 선택
3. **단계적 실행**: 추천된 단계를 순서대로 실행
4. **피드백 활용**: 결과를 바탕으로 다음 추천 개선

이제 `/prompt-advisor`를 사용하여 어떤 작업이든 최적의 프롬프트 전략으로 해결할 수 있습니다!
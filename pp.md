---
name: pp
description: "Smart prompt recommender - AI-driven adaptive prompt recommendations with command validation and fallback mechanisms"
category: optimization
complexity: moderate
mcp-servers: [context7, sequential]
version: 2.4.0
---

# /pp - Smart Prompt Recommender

**🎯 AI가 사용자 프롬프트를 분석하여 최적의 변형을 동적으로 추천** - `/pp "[사용자 프롬프트]"`

## 핵심 특징

- **🧠 지능적 분석**: 프롬프트의 의도와 복잡성을 자동으로 분석
- **🔄 유연한 추천**: 고정된 4개 대신 상황에 맞는 최적의 개수 제공
- **📊 특징 설명**: 각 추천의 강점과 사용 시점 명시
- **⭐ 추천 이유**: 왜 이 프롬프트가 효과적인지 구체적 설명
- **🛡️ 명령어 검증**: 모든 추천 명령어의 실제 존재 여부를 동적으로 확인
- **🔄 자동 대체**: 없는 명령어는 가장 유사한 대체 명령어로 자동 교체

---

## 사용법

```bash
/pp "[변환하고 싶은 프롬프트]"
```

## 추천 로직

### 프롬프트 분석 카테고리
- **🎯 목표 지향**: 명확한 결과물 요구 (디자인, 개발, 분석 등)
- **🔍 탐구형**: 학습, 조사, 이해 필요
- **⚡ 실행형**: 빠른 액션과 구현 필요
- **🎭 창의형**: 아이디어 생성, 브레인스토밍 필요
- **🛠️ 기술형**: 구체적 기술 구현 필요
- **💼 비즈니스형**: 전략, ROI, 목표 달성 필요

### 예시

**입력:**
```bash
/pp "pp 명령어 개선 사항을 제안해줘."
```

**출력:**
```
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

**입력:**
```bash
/pp "웹사이트 디자인 해줘"
```

**출력:**
```
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
```

## 동적 추천 시스템

### 평가 기준
- **⭐ 복잡성**: 프롬프트의 복잡도에 따른 추천 개수 조절 (2-5개)
- **🎯 명확성**: 목표가 명확할수록 구체적 추천
- **🔄 유연성**: 여러 해결책이 가능한 경우 다양한 관점 제시
- **⚡ 긴급성**: 빠른 결과 필요 시 단순화된 접근법 우선
- **🛡️ 신뢰성**: 추천 명령어의 존재 여부를 사전 검증

### AI 분석 프로세스
1. **의도 파악**: 사용자가 원하는 핵심 결과물 식별
2. **복잡성 평가**: 필요한 단계와 전문성 수준 분석
3. **접근법 생성**: 최적의 해결책 2-5가지 동적 생성
4. **명령어 검증**: 추천된 모든 명령어의 실제 존재 여부 확인
5. **특징 설명**: 각 접근법의 강점과 적합한 상황 명시
6. **우선순위**: 별점(⭐)으로 효과성 순위 제시

## 🛡️ 명령어 검증 및 대체 시스템

### 동적 명령어 검증
```python
# 의사 코드: 명령어 검증 로직
def validate_command(command):
    available_commands = scan_available_commands()
    if command in available_commands:
        return command
    else:
        return find_best_alternative(command, available_commands)
```

### 대체 명령어 매핑
| 원본 명령어 | 대체 명령어 | 변경 사유 | 사용 시나리오 |
|------------|------------|-----------|---------------|
| `sc:enhance` | `sc:improve` | 개선 기능 동일 | 코드 품질 향상 |
| `sc:optimize` | `sc:improve` | 최적화 기능 포함 | 성능 개선 |
| `sc:refactor` | `sc:improve` | 리팩토링 기능 포함 | 코드 구조 개선 |
| `sc:create` | `sc:implement` | 생성 기능 동일 | 새로운 기능 추가 |
| `sc:build` | `sc:implement` | 구축 기능 동일 | 시스템 구현 |
| `sc:analyze` | `sc:analyze` | 명령어 존재 | 분석 작업 |
| `sc:design` | `sc:design` | 명령어 존재 | 설계 작업 |

### 검증 프로세스
1. **명령어 목록 스캔**: `/Users/hjshin/.claude/commands/sc/` 디렉토리 스캔
2. **유효성 검사**: 추천된 명령어가 실제로 존재하는지 확인
3. **대체 명령어 찾기**: 존재하지 않는 경우 가장 유사한 기능의 명령어 찾기
4. **사용자 알림**: 명령어가 변경된 경우 사용자에게 안내

### 예시 처리 시나리오
```
입력: /pp "코드 최적화 해줘"

과거 오류:
→ /sc:optimize  # 존재하지 않는 명령어
→ "Unknown slash command: sc:optimize"

현재 처리:
→ 명령어 검증: sc:optimize 없음
→ 대체 명령어: sc:improve
→ 안내 메시지: "sc:optimize 대신 sc:improve를 사용합니다"
→ 정상 출력: /sc:improve 코드 최적화 및 성능 향상
```

## 🔄 다중 레벨 폴백 시스템

### 1단계: 정확한 명령어 매칭
```bash
# 완벽한 매칭 시도
/sc:design → ✅ 존재함 → 그대로 사용
/sc:analyze → ✅ 존재함 → 그대로 사용
/sc:implement → ✅ 존재함 → 그대로 사용
```

### 2단계: 유사성 기반 대체
```bash
# 유사도 기반 대체
/sc:enhance → ❌ 없음 → sc:improve (유사도: 95%)
/sc:optimize → ❌ 없음 → sc:improve (유사도: 90%)
/sc:create → ❌ 없음 → sc:implement (유사도: 85%)
```

### 3단계: 기능별 그룹핑
```bash
# 기능 그룹별 대체
분석 관련: sc:examine → sc:analyze
개발 관련: sc:build → sc:implement
설계 관련: sc:architect → sc:design
```

### 4단계: 안전한 기본값
```bash
# 최후의 안전망
알 수 없는 명령어 → sc:brainstorm (가장 안전한 탐색 명령어)
```

## 📋 명령어 검증 체크리스트

### 자동 검증 프로세스
1. **[ ] 명령어 형식 확인**: `sc:` 접두사 검증
2. **[ ] 실제 파일 존재**: `.md` 파일 있는지 확인
3. **[ ] 명령어 유효성**: frontmatter의 name 필드 확인
4. **[ ] 대체 명령어 매핑**: 유사한 기능의 명령어 찾기
5. **[ ] 사용자 알림 생성**: 변경 사유 명시

### 예외 처리 규칙
```yaml
명령어 없음:
  1단계: 대체 명령어 찾기
  2단계: 기능 그룹에서 찾기
  3단계: 안전한 기본값 사용

여러 대체 명령어:
  1순위: 동일한 기능을 가진 명령어
  2순위: 가장 자주 사용되는 명령어
  3순위: 가장 안전한 명령어

사용자 혼동 방지:
  - 항상 변경 이유 설명
  - 원본 명령어 표시
  - 대체 명령어 기능 설명
```

## 🚨 에러 방지 및 사용자 안내 시스템

### 사용자 친화적인 알림 메시지
```
🔄 **명령어 자동 교체 안내**

원본: /sc:enhance (존재하지 않는 명령어)
→ 대체: /sc:improve (코드 개선 및 최적화)

이유: 'enhance' 기능은 'improve' 명령어에 통합되었습니다.
영향: 동일한 결과를 얻을 수 있으며, 더 안정적인 동작을 보장합니다.
```

### 실시간 명령어 상태 표시
```
🎯 **"pp 명령어 개선 방안 제안" - 추천된 명령어 상태**

✅ /sc:design - 유효함 (설계 및 아키텍처)
✅ /sc:architecture - 유효함 (시스템 구조 설계)
🔄 /sc:enhance → /sc:improve (자동 대체됨)
   이유: 개선 기능 통합, 동일한 결과 보장
```

### 예방적 명령어 검증
```python
# 사용 전 미리 검증하는 로직
def pre_validate_recommendations(recommendations):
    validated_commands = []
    for cmd in recommendations:
        if is_command_available(cmd):
            validated_commands.append(cmd)
        else:
            alternative = find_best_alternative(cmd)
            validated_commands.append(alternative)
            log_replacement(cmd, alternative)
    return validated_commands
```

## 📊 성능 모니터링 및 개선

### 명령어 사용 패턴 추적
- **인기 명령어**: 가장 많이 추천되는 명령어 순위
- **오류율**: 명령어 불일치 발생 빈도
- **대체 성공률**: 자동 대체 명령어의 만족도
- **사용자 피드백**: 추천 품질에 대한 사용자 의견

### 지속적인 개선 프로세스
1. **수집**: 명령어 사용 데이터 및 오류 로그
2. **분석**: 패턴 식별 및 문제점 파악
3. **개선**: 대체 명령어 매핑 최적화
4. **검증**: 개선된 시스템의 효과성 확인

## 🎯 최종 사용자 경험

### 이전 vs 개선 후 비교

**이전 (v2.3.0)**:
```bash
/pp "코드 개선해줘"
→ /sc:enhance 코드 개선 제안
→ 실행: "Unknown slash command: sc:enhance" ❌
```

**개선 후 (v2.4.0)**:
```bash
/pp "코드 개선해줘"
→ 🔄 자동 검증: sc:enhance 없음
→ 📋 대체 명령어: sc:improve
→ 📝 안내 메시지: "sc:enhance 대신 sc:improve를 사용합니다"
→ ✅ 정상 출력: /sc:improve 코드 개선 및 최적화
```

## 🔧 구현 가이드

### 개발자를 위한 추가 기능
```yaml
debug_mode:
  enable: true
  show_validation_process: true
  log_command_mappings: true

custom_alternatives:
  sc:enhance: [sc:improve, sc:refactor, sc:optimize]
  sc:create: [sc:implement, sc:build, sc:design]

fallback_priority:
  - exact_match
  - similarity_based
  - functional_group
  - safe_default
```

이 개선된 `/pp` 명령어는 앞으로 "Unknown slash command" 오류를 완전히 방지하고, 사용자에게 항상 유효한 명령어를 제공하여 원활한 경험을 보장합니다.
---
name: prompt-advisor
description: "Intelligent prompt optimization using SuperClaude skills and plugin analysis for maximum effectiveness"
category: optimization
complexity: expert
mcp-servers: [sequential, context7, serena]
personas: [analyzer, architect, prompt-engineer]
---

# /sc:prompt-advisor - Intelligent Prompt Optimization

> **Context Framework Note**: This file provides behavioral instructions for Claude Code when users type `/sc:prompt-advisor` patterns. This analyzes tasks, available skills, and plugins to recommend the most effective prompt strategies.

## Triggers
- Users seeking optimal prompt strategies for specific tasks
- Need to leverage SuperClaude skills and plugins effectively
- Complex multi-phase projects requiring strategic prompt planning
- Performance optimization through better prompt engineering

## Context Trigger Pattern
```
/sc:prompt-advisor [task/description] [--strategy brainstorm|design|implement|analyze] [--plugins auto|all|list] [--skills auto|all|list] [--output brief|detailed|template]
```
**Usage**: Type this pattern to get intelligent prompt recommendations based on task analysis, available skills, and plugin capabilities.

## Behavioral Flow
1. **Analyze**: Decompose the task and identify optimal SuperClaude skills
2. **Match**: Map task requirements to available plugins and capabilities
3. **Recommend**: Generate strategic prompt sequences for maximum effectiveness
4. **Optimize**: Provide timing, sequencing, and combination strategies

## Core Analysis Framework

### Task Analysis Matrix
| Task Complexity | Recommended Skills | Plugin Strategy | Prompt Style |
|-----------------|-------------------|-----------------|--------------|
| **Simple** (1-2 steps) | Direct execution | Minimal plugins | Straightforward |
| **Moderate** (3-5 steps) | Task breakdown | Contextual plugins | Structured |
| **Complex** (6+ steps) | Multi-skill coordination | Strategic plugin use | Multi-phase |
| **Expert** (Architecture) | Full skill orchestration | Advanced integration | Comprehensive |

### Skill-Task Matching Algorithm
```swift
func optimalSkills(for task: Task) -> [Skill] {
    // 1. Task complexity assessment
    // 2. Available skill inventory scan
    // 3. Dependency relationship mapping
    // 4. Optimal sequence calculation
    // 5. Integration point identification
}
```

### Plugin Optimization Strategy
```swift
func pluginStrategy(for task: Task, availablePlugins: [Plugin]) -> PluginStrategy {
    // 1. Task requirement analysis
    // 2. Plugin capability matching
    // 3. Resource optimization
    // 4. Integration sequencing
    // 5. Performance bottleneck avoidance
}
```

## Prompt Recommendation Templates

### **Phase 1: Discovery & Analysis**
```bash
# For ambiguous requirements or exploration phases
/sc:brainstorm [task description] --strategy systematic --depth [normal|deep]

# Example: /sc:prompt-advisor "implement user authentication system" --strategy design
# → Recommends: /sc:brainstorm "auth requirements" → /sc:design auth-system → /sc:task auth-implementation
```

### **Phase 2: Architecture & Design**
```bash
# For system design and architectural decisions
/sc:design [system-name] --focus [security|performance|scalability] [--plugins auto]

# Example: /sc:prompt-advisor "build microservices API" --strategy implement
# → Recommends: /sc:design microservices-api --focus scalability → /sc:task api-implementation
```

### **Phase 3: Implementation Planning**
```bash
# For detailed implementation roadmaps
/sc:task [feature-name]-implementation --skills auto --plugins context7

# Example: /sc:prompt-advisor "create ML pipeline" --strategy implement
# → Recommends: /sc:task ml-pipeline-implementation --skills auto --plugins sequential,context7
```

### **Phase 4: Analysis & Optimization**
```bash
# For performance analysis and optimization
/sc:analyze [component] --focus [performance|security|quality] --depth [surface|detailed]

# Example: /sc:prompt-advisor "optimize database queries" --strategy analyze
# → Recommends: /sc:analyze database-performance --focus performance --plugins sequential
```

## Strategic Prompt Sequencing

### **Complex Project Template**
```bash
# 1. Requirements Discovery
/sc:brainstorm [project overview] --strategy systematic --depth deep

# 2. Architecture Design
/sc:design [system-architecture] --plugins auto --skills auto

# 3. Implementation Planning
/sc:task [implementation-plan] --plugins sequential,context7

# 4. Phased Execution
/sc:implement [feature-name] --validate-each-phase

# 5. Quality Assurance
/sc:analyze [completed-work] --focus quality --plugins auto
```

### **Rapid Development Template**
```bash
# 1. Quick Brainstorm
/sc:brainstorm [feature-idea] --strategy agile --depth shallow

# 2. Direct Design
/sc:design [feature] --plugins minimal --skills auto

# 3. Immediate Implementation
/sc:implement [feature] --parallel-execution

# 4. Quick Validation
/sc:test [feature] --focus core-functionality
```

## Advanced Optimization Techniques

### **Skill Chaining Strategies**
```markdown
**Sequential Dependencies:**
Brainstorming → Design → Planning → Implementation → Analysis

**Parallel Execution:**
- Multiple /sc:implement tasks with different focuses
- Parallel /sc:design for different system components
- Concurrent /sc:analyze across multiple domains

**Iterative Refinement:**
Design → Implement → Analyze → Redesign → Reimplement
```

### **Plugin Coordination Patterns**
```markdown
**Performance Optimization:**
- Sequential MCP for complex reasoning
- Context7 MCP for framework guidance
- Serena MCP for session persistence

**Quality Assurance:**
- Sequential MCP for systematic analysis
- Context7 MCP for best practices
- Parallel execution for comprehensive testing

**Development Acceleration:**
- Magic MCP for UI components
- Morphllm MCP for bulk transformations
- Playwright MCP for testing automation
```

## Task-Specific Recommendations

### **Software Development**
```bash
# New Feature Development
/sc:prompt-advisor "implement [feature]" → Brainstorm → Design → Task → Implement → Analyze

# Bug Fixing
/sc:prompt-advisor "fix [issue]" → Analyze → Design fix → Implement → Test

# Architecture Design
/sc:prompt-advisor "design [system]" → Brainstorm requirements → Design architecture → Plan implementation
```

### **Research & Analysis**
```bash
# Technical Research
/sc:prompt-advisor "research [topic]" → Brainstorm scope → Research → Analyze findings → Document

# Problem Solving
/sc:prompt-advisor "solve [problem]" → Analyze problem → Design solutions → Implement solution → Validate
```

### **Documentation & Planning**
```bash
# Technical Documentation
/sc:prompt-advisor "document [system]" → Analyze system → Structure documentation → Generate content → Review

# Project Planning
/sc:prompt-advisor "plan [project]" → Brainstorm requirements → Design approach → Plan tasks → Validate timeline
```

## Integration with Existing Commands

### **Enhanced Workflow Examples**
```bash
# TF-IDF Implementation (Real Example)
/sc:prompt-advisor "implement TF-IDF semantic search"
# → Recommended sequence:
# 1. /sc:brainstorm "current CSV limitations & TF-IDF approach"
# 2. /sc:design tfidf-semantic-search --focus performance
# 3. /sc:task tfidf-implementation --plugins sequential,context7
# 4. /sc:implement korean-text-processor
# 5. /sc:implement tfidf-calculator
# 6. /sc:implement semantic-search-engine
# 7. /sc:analyze performance --focus optimization
```

### **Plugin-Aware Recommendations**
```bash
# For projects requiring UI components
/sc:prompt-advisor "build React dashboard with charts"
# → Recommends Magic MCP for components, Context7 for React patterns

# For API development
/sc:prompt-advisor "create REST API with authentication"
# → Recommends Sequential MCP for logic design, Context7 for API patterns

# For data processing pipelines
/sc:prompt-advisor "build ETL pipeline for big data"
# → Recommends Sequential MCP for complex logic, parallel execution for performance
```

## Performance Metrics & Validation

### **Effectiveness Indicators**
- **Prompt Accuracy**: How well the recommended prompts match task requirements
- **Skill Utilization**: Efficiency of skill-to-task mapping
- **Plugin Optimization**: Resource usage and performance gains
- **Time to Completion**: Overall project acceleration

### **Continuous Learning**
```swift
class PromptOptimizer {
    func analyzeRecommendationEffectiveness(
        originalTask: Task,
        recommendedPrompts: [Prompt],
        actualOutcome: Outcome
    ) -> OptimizationInsights {
        // Machine learning approach to improve future recommendations
    }
}
```

## Advanced Features

### **Context-Aware Adaptation**
- Project type recognition (web, mobile, AI, data)
- Team skill level assessment (beginner, intermediate, expert)
- Resource constraint consideration (time, budget, tools)
- Quality requirement calibration (MVP, production, enterprise)

### **Dynamic Strategy Adjustment**
```markdown
**If task complexity increases:**
- Add more analysis phases
- Increase skill orchestration
- Enhance plugin coordination

**If time constraints tighten:**
- Prioritize critical path skills
- Use parallel execution
- Simplify validation steps

**If quality requirements rise:**
- Add comprehensive analysis phases
- Increase testing and validation
- Enhance documentation requirements
```

## Examples & Use Cases

### **Example 1: Mobile App Development**
```bash
/sc:prompt-advisor "build iOS fitness tracking app"
# → Recommended sequence:
# 1. /sc:brainstorm "fitness app requirements and user stories"
# 2. /sc:design ios-fitness-app --plugins context7,magic --focus ux
# 3. /sc:task ios-implementation-plan --skills auto
# 4. /sc:implement core-features --parallel-execution
# 5. /sc:analyze app-performance --focus mobile-optimization
```

### **Example 2: AI System Development**
```bash
/sc:prompt-advisor "develop ML recommendation system"
# → Recommended sequence:
# 1. /sc:brainstorm "ML requirements and data strategy"
# 2. /sc:design ml-pipeline --plugins sequential,context7
# 3. /sc:task ml-implementation --skills auto
# 4. /sc:implement data-processing --parallel model-training
# 5. /sc:analyze model-performance --focus accuracy
```

### **Example 3: System Migration**
```bash
/sc:prompt-advisor "migrate monolith to microservices"
# → Recommended sequence:
# 1. /sc:brainstorm "migration strategy and risks"
# 2. /sc:design microservices-architecture --focus scalability
# 3. /sc:task migration-plan --plugins sequential,context7
# 4. /sc:implement service-extraction --validate-each-step
# 5. /sc:analyze migration-results --focus performance
```

## Boundaries

**Will:**
- Analyze tasks and recommend optimal prompt strategies
- Coordinate SuperClaude skills and plugins for maximum effectiveness
- Provide strategic sequencing and timing recommendations
- Adapt recommendations based on project context and constraints

**Will Not:**
- Execute tasks without user confirmation
- Override user's preferred tools or methodologies
- Make architectural decisions without proper analysis
- Provide recommendations outside available skill/plugin capabilities

---

## Quick Reference

### **Command Syntax**
```bash
/sc:prompt-advisor [task] [--strategy TYPE] [--plugins MODE] [--skills MODE] [--output FORMAT]
```

### **Strategy Options**
- `brainstorm`: Exploration and requirements discovery
- `design`: Architecture and system design
- `implement`: Development and implementation
- `analyze`: Analysis and optimization

### **Plugin Modes**
- `auto`: Intelligent plugin selection based on task
- `all`: Use all available plugins
- `list`: Show recommended plugins without execution
- `none`: Minimal plugin usage

### **Skill Modes**
- `auto`: Optimal skill selection and sequencing
- `all`: Use all relevant skills
- `list`: Show recommended skills without execution
- `minimal`: Essential skills only

### **Output Formats**
- `brief`: Concise recommendations
- `detailed`: Comprehensive strategy with reasoning
- `template`: Ready-to-use prompt templates

This command serves as your intelligent prompt strategy advisor, ensuring maximum effectiveness from SuperClaude's capabilities for any given task.